---
layout: default
title: Temenos API Documentation
---

# populate

## fqn
http://temenostech.temenos.com/rels/populate

## methods
POST

## description
This type of resource is designed to provide functionality for user to populate a record for editing of which `Id` is already known. If id is not supplied it would behave same as [new](../new) i.e. it will generate the new Id and return the empty contract. 

This resource will be accessible on all T24 Application/Version by default


## uri templates
The User-Agent MUST replace every occurrence of the template parameters with a value before issuing a request for the resource.  See URI Templates [http://tools.ietf.org/html/rfc6570](http://tools.ietf.org/html/rfc6570)

`Id`	: (Optional) Query parameter provided will be used as an Id to populate a record from T24

## example
An atom representation of a link to the `populate` Customer resource
<pre>
&lt;link rel="http://www.temenos.com/rels/populate" type="application/atom+xml;type=entry" title="Customer Populate" href="Customers()/populate*{?CustomerCode=12345}*"/&gt;
</pre>

The basic structure of the http request is as follows:
<pre>
POST /T24.svc/Customers()/populate?CustomerCode=12345 HTTP/1.1
</pre>