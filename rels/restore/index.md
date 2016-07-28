---
layout: default
title: Temenos API Documentation
---

# restore

## fqn
http://rels.temenos.com/rels/restore

## methods
POST

## description
This resource is designed to provide user a capability to restore [reverse](../reverse) transaction from T24. 
 

## uri templates
The User-Agent MUST replace every occurrence of the template parameters with a value before issuing a request for the resource.  See URI Templates [http://tools.ietf.org/html/rfc6570](http://tools.ietf.org/html/rfc6570)

None


## example
An atom representation of a link to the `restore` Customer resource
<pre>
&lt;link href="Customer_Inputs('12345')/restore" rel="http://rels.temenos.com/rels/restore" type="application/atom+xml;type=entry" title="restore record" hreflang="en" length="0" /&gt;
</pre>

The basic structure of the http request is as follows:

Request
<pre>
POST /T24.svc/Customers('12345')/restore HTTP/1.1
</pre>