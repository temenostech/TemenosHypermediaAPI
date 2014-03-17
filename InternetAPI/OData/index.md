---
layout: default
title: OData
---
## Temenos Internet API (OData)

The Temenos Core API demo provide an OData service where any and every entity within the system can be accessed through the same set of URI conventions for [paging](http://docs.oasis-open.org/odata/odata/v4.0/os/part2-url-conventions/odata-v4.0-os-part2-url-conventions.html#_Toc372793863), [filtering](http://docs.oasis-open.org/odata/odata/v4.0/os/part2-url-conventions/odata-v4.0-os-part2-url-conventions.html#_Toc372793792), and even things like [zooming](http://docs.oasis-open.org/odata/odata/v4.0/os/part2-url-conventions/odata-v4.0-os-part2-url-conventions.html#_Toc372793860).  An OData service has two main entry points - the ServiceDocument and the Metadata.  For more information and examples see [http://www.odata.org/](http://www.odata.org/)


[http://t24demo.cloudapp.net/tcib-iris/TCIB.svc/](http://t24demo.cloudapp.net/tcib-iris/TCIB.svc/)
<pre>
Accept: application/atom+xml
GET http://t24demo.cloudapp.net/tcib-iris/TCIB.svc/...SomeEntity...
</pre>

[ServiceDocument](http://t24demo.cloudapp.net/tcib-iris/TCIB.svc/)
<pre>
Accept: application/atomsvc+xml
GET http://t24demo.cloudapp.net/tcib-iris/TCIB.svc/
</pre>

[$metadata](http://t24demo.cloudapp.net/tcib-iris/TCIB.svc/$metadata)
<pre>
Accept: application/xml
GET http://t24demo.cloudapp.net/tcib-iris/TCIB.svc/$metadata
</pre>

### Type Information

An OData service provides type information for EntitySet's (collections), Entity's (items), and Property's (fields) through the $metadata endpoint.

* [Hothouse.svc/$metadata](http://t24demo.cloudapp.net/tcib-iris/TCIB.svc/$metadata)


### Media types

OData flavour of Atom [application/atom+xml](http://en.wikipedia.org/wiki/Atom_(standard))





