---
layout: default
title: Temenos API Documentation
---

# new

## fqn
http://www.temenos.com/rels/new

## methods
POST

## description
This type of resource is designed to provide the next available ID for a T24 Application such as Customers or FundsTransfers.  When entering deals into T24 it would be quite onerous to expect the user to invent a new ID for each deal; it is therefore common practice for T24 Applications to provide generated IDs that can be used for the new deal, or thrown away without ever being used.  This `new` resource provides that capability by returning a populated or partially populated entity along with one or more links that could then be used to `input` or `hold` the new deal. 


## uri templates
The User-Agent MUST replace every occurrence of the template parameters with a value before issuing a request for the resource.  See URI Templates [http://tools.ietf.org/html/rfc6570](http://tools.ietf.org/html/rfc6570)

None


## example
An atom representation of a link to the new FundsTransfer resource
<pre>
&lt;link rel="http://www.temenos.com/rels/new" type="application/atom+xml;type=entry" title="New FundsTransfer" href="FundsTransfer/new"/&gt;
</pre>

The basic structure of the http request is as follows:
<pre>
POST /t24/FundsTransfer/new HTTP/1.1
Content-Length: 0
</pre>