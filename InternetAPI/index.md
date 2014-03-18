---
layout: default
title: Internet API
---
## Overview

The Temenos Internet API demo service provides an example internet bank with Retail core banking functions including Demand Deposit Accounts, Funds Transfers and Messages.

[http://t24demo.cloudapp.net/tcib-iris/](http://t24demo.cloudapp.net/tcib-iris/)

### Functional

* [Accounts](http://t24demo.cloudapp.net/tcib-iris/TCIB.svc/TcibAcctDetailss\(\))

List the internet users Accounts.
<pre>
Accept: application/atom+xml
GET http://t24demo.cloudapp.net/tcib-iris/TCIB.svc/TcibAcctDetailss()
</pre>


* [Today's Transactions for account 63002](http://t24demo.cloudapp.net/tcib-iris/TCIB.svc/TcibTxnsTodayLists\(\)?$filter=AcctId%20eq%2063002)

List Today's transactions for an Account.

<pre>
Accept: application/atom+xml
GET http://t24demo.cloudapp.net/tcib-iris/TCIB.svc/TcibTxnsTodayLists()?$filter=AcctId eq {account_id}
</pre>


* [Account Balances](http://t24demo.cloudapp.net/tcib-iris/TCIB.svc/TcibAcctBalTodays())

List the internet users Account balances

<pre>
Accept: application/atom+xml
GET http://t24demo.cloudapp.net/tcib-iris/TCIB.svc/TcibAcctBalTodays()
</pre>


* [Beneficiaries]()


* [Payments]()



### Non-Functional

Temenos Internet API supports a few types of service layouts and description formats.  We hope you can find one that suits you:

* [OData](OData)
* [Hypermedia](Hypermedia)
* [Swagger coming soon](http://t24demo.cloudapp.net/hothouse-iris/Hothouse.svc/GB0010001/api-docs.json)



#### Credentials

Temenos Internet API

* User – ANTHONYB, Password – 123456
* User – DAVIDB, Password – 123456




