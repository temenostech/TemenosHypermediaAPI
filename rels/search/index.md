---
layout: default
title: Temenos API Documentation
---

# search

## fqn
http://temenostech.temenos.com/rels/search

## methods
GET

## description
This resource is available on [root](../root) resource and user agent can use this service call as a universal search. Search can be configured on all resources. This resource will fetch data from search able database instead of transaction database. IRIS uses Solr as its search engine 


## uri templates
The User-Agent MUST replace every occurrence of the template parameters with a value before issuing a request for the resource.  See URI Templates [http://tools.ietf.org/html/rfc6570](http://tools.ietf.org/html/rfc6570)

`q`		: (MANDATORY) Query parameter which defines string to search in table

`core`	: (MANDATORY) Query parameter which defines which entity table to search


## example
An atom representation of a link to the `search` resource
<pre>
&lt;link rel="http://temenostech.temenos.com/rels/search" type="application/atom+xml;type=entry" title="search" href="search?q=Andrew&core=customer_search"/&gt;
</pre>

The basic structure of the http request is as follows:
<pre>
GET /T24.svc/search?q=Andrew&core=customer_search HTTP/1.1
</pre> 