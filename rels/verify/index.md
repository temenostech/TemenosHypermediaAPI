---
layout: default
title: Temenos API Documentation
---

# verify

## fqn
http://rels.temenos.com/rels/verify

## methods
POST

## description
This type of resource is designed to provide user with the ability to VERIFY an input-able entry within T24. 

NOTE: VERIFY operation in T24 is equivalent of EXECUTING a T24 Record.

## uri templates
The User-Agent MUST replace every occurrence of the template parameters with a value before issuing a request for the resource.  See URI Templates [http://tools.ietf.org/html/rfc6570](http://tools.ietf.org/html/rfc6570)

None

## example
An atom representation of a link to the `VERIFY` EBS.AUTO.FUNCTION resource
<pre>
&lt;link href="EbsAutoFunction_Tests('CUSTOMER.100')/verify" rel="http://rels.temenos.com/rels/verify" type="application/atom+xml;type=entry" title="verify entry" hreflang="en" length="0" /&gt;
</pre>

The basic structure of the http request is as follows:

Request
<pre>
POST /T24.svc/EbsAutoFunction_Tests('CUSTOMER.100')/verify HTTP/1.1
</pre>
