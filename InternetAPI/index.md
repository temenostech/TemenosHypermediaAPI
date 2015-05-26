---
layout: default
title: Internet API
---
## Overview

The Temenos Internet API demo service provides an example internet bank with Retail core banking functions including Demand Deposit Accounts, Funds Transfers and Messages.

[http://tcmb-demo.cloudapp.net/TCMBCommon-iris/](http://tcmb-demo.cloudapp.net/TCMBCommon-iris/)

### Functional

* [Accounts](http://tcmb-demo.cloudapp.net/TCMBCommon-iris/TCMBCommon.svc/GB0010001/enqTcibAcctDetailss\(\))

List the internet users Accounts.

<pre>
Accept: application/atom+xml	OR	Accept: application/hal+json 
GET http://tcmb-demo.cloudapp.net/TCMBCommon-iris/TCMBCommon.svc/GB0010001/enqTcibAcctDetailss()
</pre>


* [Beneficiaries](http://tcmb-demo.cloudapp.net/TCMBCommon-iris/TCMBCommon.svc/GB0010001/enqTcibBeneficiaryUtils\(\))

List the internet users Beneficiaries

<pre>
Accept: application/atom+xml	OR	Accept: application/hal+json
GET http://tcmb-demo.cloudapp.net/TCMBCommon-iris/TCMBCommon.svc/GB0010001/enqTcibBeneficiaryUtils()
</pre>

* [Payments](http://tcmb-demo.cloudapp.net/TCMBCommon-iris/TCMBCommon.svc/GB0010001/verFundsTransfer_Tcibs\(\))

The following example demonstrates how to make a payment - i.e. a Funds Transfer from One Customer account to another.

Lets assume a scenario where we want to transfer £15 in local currency account.


- **Create a new deal**

<pre>
Accept: application/atom+xml
POST http://tcmb-demo.cloudapp.net/TCMBCommon-iris/TCMBCommon.svc/GB0010001/verFundsTransfer_Tcibs()/new
</pre>


- **Fill in the information**
 
<pre>

DebitAcctNo	: 61522	[Our Account to pay from]
DebitCurrency	: GBP
DebitAmount 	: 15.0	[Make sure you remove the m:null="true" attribute from the node]
CreditAcctNo	: 64637 [Our friends Account to pay to]
CreditCurrency	: GBP
TransactionType	: AC
            
Accept: application/atom+xml
POST http://tcmb-demo.cloudapp.net/TCMBCommon-iris/TCMBCommon.svc/GB0010001/verFundsTransfer_Tcibs()
</pre>


- **Verify Transaction**

Above transaction will be automatically authorised and the results can then be seen on the recent transactions from [Temenos Internet API](InternetAPI) as normal. e.g. To access the account transaction

<pre>

User: DAVIDB, Password: 123456
Accept: application/atom+xml	OR	application/hal+json
GET http://tcmb-demo.cloudapp.net/TCMBCommon-iris/TCMBCommon.svc/GB0010001/enqTcibLastNTxnsRecentListss?$filter=AcctId eq 64637
</pre>


### Non-Functional

Temenos Internet API supports a few types of service layouts and description formats.  We hope you can find one that suits you:

* [OData](OData)
* [Hypermedia](Hypermedia)
* [API Browsers](/InternetAPIBrowsers)



#### Credentials

Temenos Internet API

* User – ROLFGERLINGTC, Password – 123456
* User – ANTHONYBTC, Password – 123456

