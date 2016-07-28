---
layout: default
title: Temenos API Documentation
---

# enrichment

## fqn
http://rels.temenos.com/rels/enrichment

## methods
GET

## description
This resource is designed to provide field enrichment to user agent for screen. This service will  be available by default for each version and can be invoked while inputting or editing a record


## uri templates
The User-Agent MUST replace every occurrence of the template parameters with a value before issuing a request for the resource.  See URI Templates [http://tools.ietf.org/html/rfc6570](http://tools.ietf.org/html/rfc6570)

`PropertyName=PropertyValue` – (MANDATORY) Query parameter provides the information about the Field in Application/Version to be enriched along with the value. If invalid/no property provided resource would return HTTP error code 400

## example
An atom representation of a link to the `enrichment` resource for FundsTransfer
<pre>
&lt;link rel="http://rels.temenos.com/rels/enrichments" type="application/atom+xml;type=entry" title="field enrichment" href="verFundsTransfer_News()/enrichment"/&gt;
</pre>

The basic structure of the http request is as follows:
<pre>
GET /T24.svc/verFundsTransfer_News()/enrichment?CustomerNo=12345 HTTP/1.1
</pre>

OR

For property belongs to a ComplexType

<pre>
GET /T24.svc/verAccount_HotOpens()/enrichment?verAccount_HotOpen_JointHolderMvGroup.verAccount_HotOpen_JointNotesSvGroup.JointNotes=1009 HTTP/1.1
</pre>