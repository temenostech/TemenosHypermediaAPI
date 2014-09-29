---
layout: default
title: Temenos API Documentation
---

# ServiceDocument

## fqn
http://schemas.microsoft.com/ado/2007/08/dataservices/related/ServiceDocument

## methods
GET

## description
This resource is available on [root](../root) resource and odata client user agent can use this service to see available Odata ServiceDocument resources.

## uri templates
The User-Agent MUST replace every occurrence of the template parameters with a value before issuing a request for the resource.  See URI Templates [http://tools.ietf.org/html/rfc6570](http://tools.ietf.org/html/rfc6570)

None

## example
An atom representation of a link to the `ServiceDocument` resource
<pre>
&lt;link href="/" rel="http://schemas.microsoft.com/ado/2007/08/dataservices/related/ServiceDocument" type="application/atom+xml;type=entry" title="ServiceDocument"&gt;&lt;/link&gt;
</pre>

The basic structure of the http request is as follows:
<pre>
GET /T24.svc/ HTTP/1.1
</pre> 