---
layout: default
title: Temenos API Documentation
---
# see

## fqn
http://temenostech.temenos.com/rels/see

## methods
GET

## description
This type of resource is designed to return the latest version of a record in T24.


## uri templates
The User-Agent MUST replace every occurrence of the template parameters with a value before issuing a request for the resource.  See URI Templates [http://tools.ietf.org/html/rfc6570](http://tools.ietf.org/html/rfc6570)

None


## example
An atom representation of a link to the `see` list resource
<pre>
&lt;link rel="http://temenostech.temenos.com/rels/see" type="application/atom+xml;type=entry" title="See Customer" href="verCustomer_Inputs('12345')/see"/&gt;
</pre>

The basic structure of the http request is as follows:
<pre>
GET /T24.svc/verCustomer_Inputs('12345')/see HTTP/1.1
</pre>