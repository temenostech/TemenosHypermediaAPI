---
layout: default
title: Internet API
---
## Overview

The Temenos Internet API demo service provides an example internet bank with Retail core banking functions including Demand Deposit Accounts, Funds Transfers and Messages.

[http://t24demo.cloudapp.net/TCMBCommon-iris/](http://t24demo.cloudapp.net/TCMBCommon-iris/)

### Functional

* [Accounts](http://t24demo.cloudapp.net/TCMBCommon-iris/TcmbCommon.svc/TcibAcctDetailss\(\))

List the internet users Accounts.

<pre>
Accept: application/atom+xml	OR	Accept: application/hal+json 
GET http://t24demo.cloudapp.net/TCMBCommon-iris/TcmbCommon.svc/TcibAcctDetailss()
</pre>


* [Today's Transactions for account 64629 (ANTHONYB)](http://t24demo.cloudapp.net/TCMBCommon-iris/TcmbCommon.svc/TcibTxnsTodayLists\(\)?$filter=AcctId%20eq%2064629)

List Today's transactions for an Account.

<pre>
Accept: application/atom+xml	OR	Accept: application/hal+json
GET http://t24demo.cloudapp.net/TCMBCommon-iris/TcmbCommon.svc/TcibTxnsTodayLists()?$filter=AcctId eq {account_id}
</pre>


* [Account Balances](http://t24demo.cloudapp.net/TCMBCommon-iris/TcmbCommon.svc/TcibAcctBalTodays\(\))

List the internet users Account balances

<pre>
Accept: application/atom+xml	OR	Accept: application/hal+json
GET http://t24demo.cloudapp.net/TCMBCommon-iris/TcmbCommon.svc/TcibAcctBalTodays()
</pre>


* [Beneficiaries](http://t24demo.cloudapp.net/TCMBCommon-iris/TcmbCommon.svc/TcibBeneficiaryUtils\(\))

List the internet users Beneficiaries

<pre>
Accept: application/atom+xml	OR	Accept: application/hal+json
GET http://t24demo.cloudapp.net/TCMBCommon-iris/TcmbCommon.svc/TcibBeneficiaryUtils()
</pre>

* [Payments]()

The following example demonstrates how to make a payment using the [Temenos Core API](/CoreAPI) - a Funds Transfer from One Customer account to another using the [Temenos Internet API](/InternetAPI) can be performed in exactly the same way.

Lets assume a scenario where Bank Customer has won a cash prize of £15 and bank is transferring money to the his/her local currency account. Bank TELLER would be performing following actions. 


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
GET http://t24demo.cloudapp.net/TCMBCommon-iris/TcmbCommon.svc/TcibTxnsTodayLists?$filter=AcctId eq 64637
</pre>


### Non-Functional

Temenos Internet API supports a few types of service layouts and description formats.  We hope you can find one that suits you:

* [OData](OData)
* [Hypermedia](Hypermedia)
* [API Browsers](/InternetAPIBrowsers)



#### Credentials

Temenos Internet API

* User – ANTHONYB, Password – 123456
* User – DAVIDB, Password – 123456




