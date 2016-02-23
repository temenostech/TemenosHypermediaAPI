---
layout: default
title: Temenos API Documentation
---

# enquiryReport

## fqn
http://temenostech.temenos.com/rels/enquiryReport

## methods
GET

## description
This command provides specialist behavior for retrieving the Enquiry Report via an Enquiry drilldown from T24.


## uri templates
The User-Agent MUST replace every occurrence of the template parameters with a value before issuing a request for the resource.  See URI Templates [http://tools.ietf.org/html/rfc6570](http://tools.ietf.org/html/rfc6570)

None


## example
An atom representation of a link to the `enquiryReport` Fundstransfer deal
<pre>
&lt;link href="verFundsTransfers('FTXXXXXX')/enquiryReport" rel="http://temenostech.temenos.com/rels/enquiryReport" type="application/atom+xml;type=entry" title="Preview deal" hreflang="en" length="0" /&gt;
</pre>

The basic structure of the http request is as follows:

Request
<pre>
GET /T24.svc/verFundsTransfers('FTXXXXXX')/enquiryReport HTTP/1.1
</pre>