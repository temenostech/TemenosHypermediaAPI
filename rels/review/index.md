---
layout: default
title: Temenos API Documentation
---

# review

## fqn
http://temenostech.temenos.com/rels/review

## methods
GET

## description
TBA

## uri templates
The User-Agent MUST replace every occurrence of the template parameters with a value before issuing a request for the resource.  See URI Templates [http://tools.ietf.org/html/rfc6570](http://tools.ietf.org/html/rfc6570)

None


## example
An atom representation of a link to the `review` Customer resource
<pre>
&lt;link href="Customer_Inputs('12345')/review" rel="http://temenostech.temenos.com/rels/review" type="application/atom+xml;type=entry" title="review record" hreflang="en" length="0" /&gt;
</pre>

The basic structure of the http request is as follows:

Request
<pre>
GET /T24.svc/Customers('12345')/review HTTP/1.1
</pre>