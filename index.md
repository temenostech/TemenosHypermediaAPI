---
layout: default
title: Temenos API
---
## Welcome

Temenos is pleased to offer you access to the Temenos Internet API (see [Temenos Connect Internet](http://www.temenos.com/en/products-and-services/front-end--channels/temenos-connect/temenos-connect-internet/)) and the Temenos Core API.  Built on T24 and the [IRIS](http://www.rimdsl.org) interaction framework, these Internet and Core endpoints support both Data and Interaction Services.



### Temenos Internet API

The Temenos Internet API demo service provides an example internet bank with Retail core banking functions including Demand Deposit Accounts, Funds Transfers and Messages.  

[http://t24demo.cloudapp.net/tcib-iris/](http://t24demo.cloudapp.net/tcib-iris/)

* [OData](http://t24demo.cloudapp.net/tcib-iris/TCIB.svc/)
* Hypermedia (coming soon)


### Temenos Core API

The Temenos Core API demo service provides an example of internal banking employees API.  A Retail core banking employee can access a wide array of core banking functions and maintenance services.

[http://t24demo.cloudapp.net/hothouse-iris/](http://t24demo.cloudapp.net/hothouse-iris/)

* [OData](http://t24demo.cloudapp.net/hothouse-iris/Hothouse.svc/)
* [Hypermedia](http://t24demo.cloudapp.net/hothouse-iris/Hothouse.svc/root)


#### Documentation

Temenos API documentation is available in several different formats.

***OData metadata***

An OData service documents the available services with a $metadata document.

* [TCIB.svc/$metadata](http://t24demo.cloudapp.net/tcib-iris/TCIB.svc/$metadata)
* [Hothouse.svc/$metadata](http://t24demo.cloudapp.net/hothouse-iris/Hothouse.svc/$metadata)


***Link relations***

Our Hypermedia services are designed to be self describing and documented with dereferenceable URI's.

[TemenosHypermediaAPI](rels)


***Swagger***

Coming soon.



#### Credentials

Temenos Internet API

* User – ANTHONYB, Password – 123456
* User – DAVIDB, Password – 123456


Back Office Users

* User – SSOUSER1, Password – 123456
* User – SSOUSER2, Password – 123456




### Media types

#### OData (application/atom+xml)


#### HAL (application/hal+json or application/hal+xml)





