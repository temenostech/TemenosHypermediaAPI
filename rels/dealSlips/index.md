---
layout: default
title: Temenos API Documentation
---

# dealSlips

## fqn
http://rels.temenos.com/rels/dealSlips

## methods
GET

## description
This command provides specialist behavior for retrieving deal slips, from T24, associated with deal slip ids stored in the IRIS interaction context by a previous action such as authorize.


## uri templates
The User-Agent MUST replace every occurrence of the template parameters with a value before issuing a request for the resource.  See URI Templates [http://tools.ietf.org/html/rfc6570](http://tools.ietf.org/html/rfc6570)

None


## example
An atom representation of a link to the `dealSlips` Fundstransfer deal
<pre>
&lt;link href="verFundsTransfers('FTXXXXXX')/dealSlips" rel="http://rels.temenos.com/rels/dealSlips" type="application/atom+xml;type=entry" title="Preview deal" hreflang="en" length="0" /&gt;
</pre>

The basic structure of the http request is as follows:

Request
<pre>
GET /T24.svc/verFundsTransfers('FTXXXXXX')/dealSlips HTTP/1.1
</pre>