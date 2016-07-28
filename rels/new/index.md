---
layout: default
title: Temenos API Documentation
---

# new

## fqn
http://rels.temenos.com/rels/new

## methods
POST

## description
This type of resource is designed to provide the next available ID for a T24 Application such as Customers or FundsTransfers.  When entering deals into T24 it would be quite onerous to expect the user to invent a new ID for each deal; it is therefore common practice for T24 Applications to provide generated IDs that can be used for the new deal, or thrown away without ever being used.  This `new` resource provides that capability by returning a populated or partially populated entity along with one or more links that could then be used to [input](../input) or [hold](../hold) the new deal. 


## uri templates
The User-Agent MUST replace every occurrence of the template parameters with a value before issuing a request for the resource.  See URI Templates [http://tools.ietf.org/html/rfc6570](http://tools.ietf.org/html/rfc6570)

`Id`	: Query parameter containing Entity Id field which can be passed if user agent user would like to override auto id generation. `MANDATORY` if Application/Version DOES NOT support AUTO.ID else it is `OPTIONAL`


## example
An atom representation of a link to the new FundsTransfer resource
<pre>
&lt;link rel="http://rels.temenos.com/rels/new" type="application/atom+xml;type=entry" title="New FundsTransfer" href="FundsTransfers()/new*{?RefNo=FT00100001}*"/&gt;
</pre>

The basic structure of the http request is as follows:
<pre>
POST /T24.svc/FundsTransfers()/new HTTP/1.1
Content-Length: 0
</pre>