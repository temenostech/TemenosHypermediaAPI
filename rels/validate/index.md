---
layout: default
title: Temenos API Documentation
---

# validate

## fqn
http://rels.temenos.com/rels/validate

## methods
POST

## description
This type of resource is designed to provide user with the ability to validate input-able entry with T24 before it tries to use [input](../input)

This resource would return validation errors or overrides if there are any else would return fully populated entry. 


## uri templates
The User-Agent MUST replace every occurrence of the template parameters with a value before issuing a request for the resource.  See URI Templates [http://tools.ietf.org/html/rfc6570](http://tools.ietf.org/html/rfc6570)

None


## example
An atom representation of a link to the authorise Customer resource
<pre>
&lt;link href="Customer_Inputs()/validate" rel="http://rels.temenos.com/rels/validate" type="application/atom+xml;type=entry" title="validate enttry" hreflang="en" length="0" /&gt;
</pre>

The basic structure of the http request is as follows:

Request
<pre>
POST /T24.svc/Customers('100226')/validate HTTP/1.1
</pre>
