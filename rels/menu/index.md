---
layout: default
---

# menu

## fqn
http://www.temenos.com/rels/menu

## methods
GET

## description
This type of resource is designed to provide a user navigation capability.  This `menu` resource provides that capability by returning an entity with zero or more links that could then be used to perform any of the various requests to T24. 


## uri templates
The User-Agent MUST replace every occurrence of the template parameters with a value before issuing a GET for the resource.  See URI Templates [http://tools.ietf.org/html/rfc6570](http://tools.ietf.org/html/rfc6570)

None


## example
An atom representation of a link to the user menu resource
<pre>
&lt;link href="usermenu" rel="http://www.temenos.com/rels/menu" type="application/atom+xml;type=entry" title="User Menu" hreflang="en" length="0" /&gt;
</pre>

The basic structure of the http request is as follows:
<pre>
GET /t24/usermenu HTTP/1.1
</pre>