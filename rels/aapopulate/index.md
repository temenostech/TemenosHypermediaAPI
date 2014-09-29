---
layout: default
title: Temenos API Documentation
---

# aapopulate

## fqn
http://temenostech.temenos.com/rels/aapopulate

## methods
POST

## description
This is a special type of resource which is only applicable on AAA versions of T24. This resource is equivalent of first time validation of an AAA deal in Browser. This resource will return all nested AAA property classes along with their properties for user. 

**NOTE:** This resource will only be available for AAA versions.


## uri templates
The User-Agent MUST replace every occurrence of the template parameters with a value before issuing a request for the resource.  See URI Templates [http://tools.ietf.org/html/rfc6570](http://tools.ietf.org/html/rfc6570)

None

## example
An atom representation of a link to the `populate` Customer resource
<pre>
&lt;link rel="http://www.temenos.com/rels/aapopulate" type="application/atom+xml;type=entry" title="AAA Populate" href="verAaArrangementActivity_AaNews('AA123456')/aapopulate"/&gt;
</pre>

The basic structure of the http request is as follows:
<pre>
POST /T24.svc/verAaArrangementActivity_AaNews('AA123456')/aapopulate HTTP/1.1
</pre>