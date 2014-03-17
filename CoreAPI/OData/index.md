---
layout: default
title: OData
---
## Temenos Core API (OData)

The Temenos Core API demo provide an OData service where any and every entity within the system can be accessed through the same set of URI conventions for [paging](http://docs.oasis-open.org/odata/odata/v4.0/os/part2-url-conventions/odata-v4.0-os-part2-url-conventions.html#_Toc372793863), [filtering](http://docs.oasis-open.org/odata/odata/v4.0/os/part2-url-conventions/odata-v4.0-os-part2-url-conventions.html#_Toc372793792), and even things like [zooming](http://docs.oasis-open.org/odata/odata/v4.0/os/part2-url-conventions/odata-v4.0-os-part2-url-conventions.html#_Toc372793860).  An OData service has two main entry points - the ServiceDocument and the Metadata.  For more information and examples see [http://www.odata.org/](http://www.odata.org/)


[http://t24demo.cloudapp.net/hothouse-iris/Hothouse.svc/GB0010001/](http://t24demo.cloudapp.net/hothouse-iris/Hothouse.svc/GB0010001/)
<pre>
Accept: application/atom+xml
GET http://t24demo.cloudapp.net/hothouse-iris/Hothouse.svc/GB0010001/...SomeEntity...
</pre>

[ServiceDocument](http://t24demo.cloudapp.net/hothouse-iris/Hothouse.svc/GB0010001/)
<pre>
Accept: application/atomsvc+xml
GET http://t24demo.cloudapp.net/hothouse-iris/Hothouse.svc/GB0010001/
</pre>

[$metadata](http://t24demo.cloudapp.net/hothouse-iris/Hothouse.svc/GB0010001/$metadata)
<pre>
Accept: application/xml
GET http://t24demo.cloudapp.net/hothouse-iris/Hothouse.svc/GB0010001/$metadata
</pre>

### Type Information

An OData service provides type information for EntitySet's (collections), Entity's (items), and Property's (fields) through the $metadata endpoint.

* [Hothouse.svc/$metadata](http://t24demo.cloudapp.net/hothouse-iris/Hothouse.svc/GB0010001/$metadata)


### Media types

OData flavour of Atom [application/atom+xml](http://en.wikipedia.org/wiki/Atom_(standard))





