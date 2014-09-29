---
layout: default
title: Temenos API Documentation
---

# root

## fqn
http://temenostech.temenos.com/rels/root

## methods
GET

## description
This is considered as a first service to be called from user agent to get the links available for rest of the interaction. This service will offer links to call OData [ServiceDocument](ServiceDocument), [profile](profile), [search](search) and [menu](menu)


## uri templates
The User-Agent MUST replace every occurrence of the template parameters with a value before issuing a request for the resource.  See URI Templates [http://tools.ietf.org/html/rfc6570](http://tools.ietf.org/html/rfc6570)

None

## example
An atom representation of a link to the `root` resource
<pre>
&lt;link rel="http://temenostech.temenos.com/rels/root" type="application/atom+xml;type=entry" title="service root" href="root"/&gt;
</pre>

The basic structure of the http request is as follows:
<pre>
GET /T24.svc/root HTTP/1.1
</pre>