---
layout: default
title: Temenos API Documentation
---

# paste

## fqn
http://rels.temenos.com/rels/paste

## methods
POST

## description
This type of resource is designed to expose T24 clipboard functionality to REST user agent. User agent can call this resource to retrieve data which was copied using [copy](../copy) resource

This resource is equivalent of [new](../new) resource where it will generate the new Id if applicable, default values with an addition to fill/overwrite Application/Version entity properties with copied data


## uri templates
The User-Agent MUST replace every occurrence of the template parameters with a value before issuing a request for the resource.  See URI Templates [http://tools.ietf.org/html/rfc6570](http://tools.ietf.org/html/rfc6570)

`Id`	: Query parameter containing Entity Id field which can be passed if user agent user would like to override auto id generation. `MANDATORY` if Application/Version DOES NOT support AUTO.ID else it is `OPTIONAL`

## example
An atom representation of a link to the `paste` Customer resource
<pre>
&lt;link rel="http://rels.temenos.com/rels/paste" type="application/atom+xml;type=entry" title="Copy deal" href="verCustomer_Inputs()/paste*{?CustomerCode=12345}*"/&gt;
</pre>

The basic structure of the http request is as follows:
<pre>
POST /T24.svc/verCustomer_Inputs()/paste HTTP/1.1
</pre>