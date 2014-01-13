---
layout: default
---

# delete

## fqn
http://www.temenos.com/rels/delete

## methods
DELETE

## description
This type of resource is designed to remove or mark items for deletion.  When managing deals within T24 it often necessary or desirable to maintain data for a relatively short period.  This `delete` resource provides that removal / deletion capability. 


## uri templates
The User-Agent MUST replace every occurrence of the template parameters with a value before issuing a request for the resource.  See URI Templates [http://tools.ietf.org/html/rfc6570](http://tools.ietf.org/html/rfc6570)

None


## example
An atom representation of a link to the delete Customer resource
<pre>
&lt;link rel="http://www.temenos.com/rels/delete" type="application/atom+xml;type=entry" title="Delete Customer" href="Customers('123')"/&gt;
</pre>

The basic structure of the http request is as follows:
<pre>
DELETE /t24/Customers('123') HTTP/1.1
</pre>