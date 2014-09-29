---
layout: default
title: Temenos API Documentation
---

# copy

## fqn
http://temenostech.temenos.com/rels/copy

## methods
POST

## description
This type of resource is designed to expose T24 clipboard functionality to REST user agent. User agent can call this resource to save its contract which it can [paste](paste) later to populate new contracts quickly.


## uri templates
The User-Agent MUST replace every occurrence of the template parameters with a value before issuing a request for the resource.  See URI Templates [http://tools.ietf.org/html/rfc6570](http://tools.ietf.org/html/rfc6570)

None

## example
An atom representation of a link to the `copy` Customer resource
<pre>
&lt;link rel="http://temenostech.temenos.com/rels/copy" type="application/atom+xml;type=entry" title="Copy deal" href="verCustomer_Inputs('12345')/copy"/&gt;
</pre>

The basic structure of the http request is as follows:
<pre>
POST /T24.svc/verCustomer_Inputs('12345')/copy HTTP/1.1
</pre>