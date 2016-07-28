---
layout: default
title: Temenos API Documentation
---

# input

## fqn
http://rels.temenos.com/rels/hold

## methods
POST

## description
This type of resource is designed to provide a user with the ability to store `new` or modified entries into hold status in T24.

User should be able to retrieve the saved data at any point of time afterwards for modification and should be able to perform normal commit on it using [input](../input) resource. 


## uri templates
The User-Agent MUST replace every occurrence of the template parameters with a value before issuing a request for the resource.  See URI Templates [http://tools.ietf.org/html/rfc6570](http://tools.ietf.org/html/rfc6570)

None


## example
An atom representation of a link to the `hold` Customer resource
<pre>
&lt;link href="Customer_Inputs('12345')/hold" rel="http://rels.temenos.com/rels/hold" type="application/atom+xml;type=entry" title="hold record" hreflang="en" length="0" /&gt;
</pre>

The basic structure of the http request is as follows:

Request
<pre>
POST /T24.svc/Customers('12345')/hold HTTP/1.1
</pre>