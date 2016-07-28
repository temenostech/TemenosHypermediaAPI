---
layout: default
title: Temenos API Documentation
---

# changedValues

## fqn
http://rels.temenos.com/rels/changedValues

## methods
GET

## description
This type of resource is designed to provide difference (delta fields) between LIVE and NAU record of T24

## uri templates
The User-Agent MUST replace every occurrence of the template parameters with a value before issuing a request for the resource.  See URI Templates [http://tools.ietf.org/html/rfc6570](http://tools.ietf.org/html/rfc6570)

None

## example
An atom representation of a link to the `changedValues` Customer_Inputs deal
<pre>
&lt;link href="verCustomer_Inputs('12345')/changedValues" rel="http://rels.temenos.com/rels/changedValues" type="application/atom+xml;type=entry" title="Get changed values" hreflang="en" length="0" /&gt;
</pre>

The basic structure of the http request is as follows:

Request
<pre>
GET /T24.svc/verCustomer_Inputs('12345')/changedValues HTTP/1.1
</pre>