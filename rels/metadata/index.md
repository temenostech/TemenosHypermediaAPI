---
layout: default
---

#metadata

## fqn
http://www.temenos.com/rels/metadata

## methods
POST

## description
This type of resource is designed to provide a runtime metadata for each field present in a T24 Application such as Customers or FundsTransfers. When entering deals into T24 on the basis of information provided in an particular field can change the behaviour of the other dependent fields i.e. can make them NOINPUT/READONLY etc.

This type resource can be very useful for a user agent to render the screen with the updated metadata information.

This `metdata` resource provides that capability by returning a `Feed` of T24FieldMetadata entity containing following information;

`Id`	: Fully qualified name 

`Entity`: Entity name

`Property`: Property name

 `Visible`: Visibility of the property

`Mandatory`: If its mandatory

`MandatorySelection`: If mandatory selection field

`ReadOnly`: If its readonly

`PrimaryKey`: If its a primary key

`PossibleValues`: List Enumerations

## uri templates
The User-Agent MUST replace every occurrence of the template parameters with a value before issuing a request for the resource.  See URI Templates [http://tools.ietf.org/html/rfc6570](http://tools.ietf.org/html/rfc6570)

None


## example
An atom representation of a link to the new FundsTransfer resource
<pre>
&lt;link rel="http://www.temenos.com/rels/metadata" type="application/atom+xml;type=entry" title="T24FieldMetadata" href="T24FieldMetadata"/&gt;
</pre>

The basic structure of the http request is as follows:
<pre>
POST /t24/T24FieldMetadata HTTP/1.1
Content-Length: 0
</pre>