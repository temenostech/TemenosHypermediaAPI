---
layout: default
title: Hypermedia
---
## Temenos Internet API (Hypermedia)

The Temenos Internet API demo provides an Hypermedia service where a path through the system and available options are communicated entirely by links and [link relations](http://tools.ietf.org/html/rfc5988).  Once a collection in the system has been reached we use the OData URI conventions for [paging](http://docs.oasis-open.org/odata/odata/v4.0/os/part2-url-conventions/odata-v4.0-os-part2-url-conventions.html#_Toc372793863), [filtering](http://docs.oasis-open.org/odata/odata/v4.0/os/part2-url-conventions/odata-v4.0-os-part2-url-conventions.html#_Toc372793792), and [zooming](http://docs.oasis-open.org/odata/odata/v4.0/os/part2-url-conventions/odata-v4.0-os-part2-url-conventions.html#_Toc372793860).


Service endpoint coming soon.



### Link relations

Our Hypermedia services are designed to be self describing and documented with dereferenceable URI's.

[TemenosHypermediaAPI](/rels)


### Type Information

If you need a type system you can use the OData type information for EntitySet's (collections), Entity's (items), and Property's (fields) through the $metadata endpoint.

* [Hothouse.svc/$metadata](http://t24demo.cloudapp.net/TCMBCommon-iris/TcmbCommon.svc/$metadata)


### Media types (supporting links)

OData flavour of Atom [application/atom+xml](http://en.wikipedia.org/wiki/Atom_(standard))


HAL [application/hal+json or application/hal+xml](http://stateless.co/hal_specification.html)


