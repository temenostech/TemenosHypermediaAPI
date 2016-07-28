---
layout: default
title: Temenos API Documentation
---

# deliveryPreview

## fqn
http://rels.temenos.com/rels/deliveryPreview

## methods
POST

## description
This commands initializes a T24 delivery preview workflow including triggering the generation of the delivery preview data in T24


## uri templates
The User-Agent MUST replace every occurrence of the template parameters with a value before issuing a request for the resource.  See URI Templates [http://tools.ietf.org/html/rfc6570](http://tools.ietf.org/html/rfc6570)

None


## example
An atom representation of a link to the `deliveryPreview` Fundstransfer deal
<pre>
&lt;link href="verFundsTransfers('FTXXXXXX')/deliveryPreview" rel="http://rels.temenos.com/rels/deliveryPreview" type="application/atom+xml;type=entry" title="Preview deal" hreflang="en" length="0" /&gt;
</pre>

The basic structure of the http request is as follows:

Request
<pre>
POST /T24.svc/verFundsTransfers('FTXXXXXX')/deliveryPreview HTTP/1.1
</pre>