---
layout: default
title: Temenos API Documentation
---

# input

## fqn
http://www.temenos.com/rels/input

## methods
GET, POST

## description
This type of resource is designed to provide a user with the ability to store `new` deals or modify existing deals within T24.  When managing deals within T24 it is often necessary to store deals and modify deals at the same time as other users.  This `input` resource provides that capability by allowing the user to GET an existing deal with an ETAG value and POST to store the deal with the 'If-Match' precondition providing the same ETAG value.  This ensures that the deal modified by the user is the most up to date version of the deal within T24. 


## uri templates
The User-Agent MUST replace every occurrence of the template parameters with a value before issuing a request for the resource.  See URI Templates [http://tools.ietf.org/html/rfc6570](http://tools.ietf.org/html/rfc6570)

None


## example
An atom representation of a link to the authorise Customer resource
<pre>
&lt;link href="Customer_Inputs()" rel="http://schemas.microsoft.com/ado/2007/08/dataservices/related/Customer_Inputs http://www.temenos.com/rels/input" type="application/atom+xml;type=entry" title="input" hreflang="en" length="0" /&gt;
</pre>

The basic structure of the http request is as follows:

Request
<pre>
GET /t24/Customers('100226') HTTP/1.1
</pre>

Response
<pre>
ETag: "686897696a7c876b7e"
</pre>

Request
<pre>
POST /t24/Customers('100226') HTTP/1.1
If-Match: "686897696a7c876b7e"
&lt;?xml version='1.0' encoding='UTF-8'?&gt;
&lt;entry 
    xmlns="http://www.w3.org/2005/Atom" 
    xmlns:d="http://schemas.microsoft.com/ado/2007/08/dataservices" 
    xmlns:m="http://schemas.microsoft.com/ado/2007/08/dataservices/metadata" xml:base="http://localhost:9081/hothouse-iris/Hothouse.svc/"&gt;
    &lt;id&gt;http://localhost:9081/hothouse-iris/Hothouse.svc/Customer_Inputs()/new&lt;/id&gt;
    &lt;title type="text"&gt;&lt;/title&gt;
    &lt;updated&gt;2014-01-13T15:51:11Z&lt;/updated&gt;
...
</pre>