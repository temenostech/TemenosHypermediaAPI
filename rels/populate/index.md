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
This type of resource is designed to provide functionality required for each Application/Version in T24 by supplying links to all possible resources (if applicable) like `New Deal`, `List of Live Record`, `List of IAuth Records` etc upon launching the application/version. In other terms it will act as landing page for each Application/Version in T24. 

This resource will be accessible on all T24 Application/Version by default


## uri templates
The User-Agent MUST replace every occurrence of the template parameters with a value before issuing a request for the resource.  See URI Templates [http://tools.ietf.org/html/rfc6570](http://tools.ietf.org/html/rfc6570)

None

## example
An atom representation of a link to the `populate` Customer resource
<pre>
&lt;link rel="http://www.temenos.com/rels/populate" type="application/atom+xml;type=entry" title="Customer Populate" href="Customers()/populate"/&gt;
</pre>

The basic structure of the http request is as follows:
<pre>
POST /T24.svc/Customers()/populate HTTP/1.1
</pre>