---
layout: default
title: Temenos API Documentation
---

# contract

## fqn
http://temenostech.temenos.com/rels/contract

## methods
GET

## description
TBA


## uri templates
The User-Agent MUST replace every occurrence of the template parameters with a value before issuing a request for the resource.  See URI Templates [http://tools.ietf.org/html/rfc6570](http://tools.ietf.org/html/rfc6570)

## example
An atom representation of a link to the `contract` Customer resource
<pre>
&lt;link rel="http://www.temenos.com/rels/contract" type="application/atom+xml;type=entry" title="Customer Contract" href="Customers()/contract"/&gt;
</pre>

The basic structure of the http request is as follows:
<pre>
GET /T24.svc/Customers()/contract HTTP/1.1
</pre>