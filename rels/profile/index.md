---
layout: default
title: Temenos API Documentation
---

# profile

## fqn
http://temenostech.temenos.com/rels/profile

## methods
GET

## description
This resource is available on [root](../root) resource and user agent is expected to call this resource to load user profile. 


## uri templates
The User-Agent MUST replace every occurrence of the template parameters with a value before issuing a request for the resource.  See URI Templates [http://tools.ietf.org/html/rfc6570](http://tools.ietf.org/html/rfc6570)

None

## example
An atom representation of a link to the `profile` resource
<pre>
&lt;link rel="http://temenostech.temenos.com/rels/profile" type="application/atom+xml;type=entry" title="User Profile" href="/profile"/&gt;
</pre>

The basic structure of the http request is as follows:
<pre>
GET /T24.svc/profile HTTP/1.1
</pre>  