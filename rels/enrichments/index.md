---
layout: default
title: Temenos API Documentation
---

# enrichments

## fqn
http://temenostech.temenos.com/rels/enrichments

## methods
GET

## description
This resource is designed to provide field enrichments to user agent for screen. This service will  be available where applicable i.e. while inputting or editing a record


## uri templates
The User-Agent MUST replace every occurrence of the template parameters with a value before issuing a request for the resource.  See URI Templates [http://tools.ietf.org/html/rfc6570](http://tools.ietf.org/html/rfc6570)

`Field` – (MANDATORY) Query parameter provides the information about the Field in Application/Version to be enriched

`FieldValue` - (MANDATORY) Query parameter is provides the information about the Field value should be used for Enrichment 

## example
An atom representation of a link to the `enrichments` resource for FundsTransfer
<pre>
&lt;link rel="http://temenostech.temenos.com/rels/enrichments" type="application/atom+xml;type=entry" title="field enrichments" href="verFundsTransfer_News()/enrichments"/&gt;
</pre>

The basic structure of the http request is as follows:
<pre>
GET /T24.svc/verFundsTransfer_News()/enrichments?Field=CustomerNo&FieldValue=12345 HTTP/1.1
</pre>