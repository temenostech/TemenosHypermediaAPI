---
layout: default
title: Temenos API
---
## Welcome

Temenos is pleased to offer you access to the Temenos Internet API (see [Temenos Connect Internet](http://www.temenos.com/en/products-and-services/front-end--channels/temenos-connect/temenos-connect-internet/)) and the Temenos Core API.  Built on T24 and the [IRIS](http://www.rimdsl.org) interaction framework, these Internet and Core endpoints support both Data and Interaction Services.



### Temenos Internet API

The Temenos Internet API demo service provides an example internet bank with Retail core banking functions including Demand Deposit Accounts, Funds Transfers and Messages.  

[http://t24demo.cloudapp.net/tcib-iris/](http://t24demo.cloudapp.net/tcib-iris/)

* [Documentation](InternetAPI)
* [API Browsers](InternetAPIBrowsers)

#### Temenos Legacy Internet User Interface

The Temenos Legacy Internet User Interface is an servlet based application which uses client server connectivity architecture bases on JCA to directly communicate with T24 server. This interface provide functionality to perform Retail core banking functions including Demand Deposit Accounts, Funds Transfers and Messages for a Internet banking user.  

[http://t24demo.cloudapp.net/ARC-IB](http://t24demo.cloudapp.net/ARC-IB)

##### Credentials


- User - MICKROSS, Password - 123456, PIN - [LEAVE_BLANK]

### Temenos Core API

The Temenos Core API demo service provides an example of internal banking employees API.  A Retail core banking employee can access a wide array of core banking functions and maintenance services.

[http://t24demo.cloudapp.net/hothouse-iris/](http://t24demo.cloudapp.net/hothouse-iris//Hothouse.svc/GB0010001/)

* [Documentation](CoreAPI)
* [API Browsers](CoreAPIBrowsers)

### Temenos Core User Agent

The Temenos Core User Agent is a browser based user agent which consumes services hosted by [Temenos Core API](CoreAPI) along with the new fresh look and feel. This interface is for a Retail core banking employee for their day to day work

[http://t24demo.cloudapp.net/DashBoardDynamic](http://t24demo.cloudapp.net/DashBoardDynamic)

##### Credentials

- User - DASHDYNAMIC, Password - 123456

#### Temenos Legacy Core User Interface

The Temenos Legacy Core User interface is a servlet based application which uses client server connectivity architecture bases on JCA to directly communicate with T24 server. This interface is for a Retail core banking employee for their day to day work

[http://t24demo.cloudapp.net/BrowserWeb](http://t24demo.cloudapp.net/BrowserWeb)

##### Credentials

- User - RETAILUSER, Password - 123456


### Performing Funds Transfer

Currently this functionality can be used from [Temenos Core API](CoreAPI). So lets assume a scenario where Bank Customer has won a cash prize of £15 and bank is transferring money to the his/her local currency account. Bank TELLER would be performing following actions. 

NOTE: This is an example of Funds Transfer and this can be done from One Customer account to another exactly the same way from the [Temenos Internet API](InternetAPI) which we are currently HACKING!

To access the [Temenos Core API](CoreAPI) using credentials as UserName: SSOUSER1, Password: 123456

- **Create a new deal**

<pre>
Accept: application/atom+xml
POST http://t24demo.cloudapp.net/hothouse-iris/Hothouse.svc/FundsTransfer_Edges()/new
</pre>


- **Fill in the information**
 
<pre>

DebitAcctNo		: 61522	[Bank's Internal Account to payout prizes]
DebitCurrency	: GBP
DebitAmount 	: 15.0	[Make sure you remove the m:null="true" attribute from the node]
CreditAcctNo	: 64637 [Bank Customer who won the prize]
CreditCurrency	: GBP
TransactionType	: AC
            
Accept: application/atom+xml
POST http://t24demo.cloudapp.net/hothouse-iris/Hothouse.svc/FundsTransfer_Edges()
</pre>

- **Accept OVERRIDE**

Above request will be responded with the WARNING message which is referred as OVERRIDE in T24. Accept the OVERRIDE by copying the value returned in 'Error_Messages > element > Code' attribute and append into the following element present in the actual request and send it again to the collection; 

<pre>
FundsTransfer_Edge_OverrideMvGroup > element > Override > ACCT.UNAUTH.OD

Accept: application/atom+xml
POST http://t24demo.cloudapp.net/hothouse-iris/Hothouse.svc/FundsTransfer_Edges()
</pre>

- **Authorise A Deal**

T24 has concept of **Four(4) Eyes Authorisation** where one person INPUT and other person with more access rights in the system should be able to authorise a deal. So access the following service with different credentials.
User = SSOUSER2, Password = 123456 (Hacking from branch TELLER to Branch Manager let say) to see the UNAUTH record 

<pre>
Accept: application/atom+xml
GET http://t24demo.cloudapp.net/hothouse-iris/Hothouse.svc/FundsTransfer_EdgesIAuth('RefNo')
</pre>
Note: Update the RefNo with the actual reference

Above will return the UNAUTH record from T24 with one special entry in the HEADER called 'ETag', copy the value and set it as follows; 

<pre>
If-Match: "ETag"
Accept: application/atom+xml
PUT http://t24demo.cloudapp.net/hothouse-iris/Hothouse.svc/FundsTransfer_EdgesIAuth('RefNo')/authorise
</pre>
Note: Update the RefNo with the actual reference

- **Verify Transaction**

Above will be authorise the deal and perform the real transaction within T24 which can then be seen on Customer account as recent transaction from [Temenos Internet API](InternetAPI) as normal. To access Customer transaction access the link as follows; 

<pre>

User: DAVIDB, Password: 123456
Accept: application/atom+xml	OR	application/hal+json
GET http://t24demo.cloudapp.net/tcib-iris/TCIB.svc/TcibTxnsTodayLists?$filter=AcctId eq 64637
</pre>