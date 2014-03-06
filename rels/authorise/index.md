---
layout: default
title: Temenos API Documentation
---

# authorise

## fqn
http://www.temenos.com/rels/authorise

## methods
POST

## description
This type of resource is designed to provide a deal approval facility for a T24 Application.  When entering deals into T24 it is common practice to require an additional user to authorise the newly `input` deal.  This `authorise` resource provides that capability by allowing the second user to POST their approval. 


## uri templates
The User-Agent MUST replace every occurrence of the template parameters with a value before issuing a request for the resource.  See URI Templates [http://tools.ietf.org/html/rfc6570](http://tools.ietf.org/html/rfc6570)

None


## example
An atom representation of a link to the authorise Customer resource
<pre>
&lt;link rel="http://www.temenos.com/rels/authorise" type="application/atom+xml;type=entry" title="Authorise Customer" href="CustomersIAuth('100226')"/&gt;
</pre>

The basic structure of the http request is as follows:
<pre>
POST /t24/CustomersIAuth('100226') HTTP/1.1
</pre>