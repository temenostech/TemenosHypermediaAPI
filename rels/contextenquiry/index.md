---
layout: default
---
# contextenquiry

## fqn
http://www.temenos.com/rels/contextenquiry

## methods
GET

## description
This type of resource is designed to return a number of enquiries associated with one or more fields on the screen.  When entering data into a form it is often useful to drill down to more detailed information about a particular value within that form.  This `contextenquiry` link provides that capability by providing the name or names of the fields in the query parameters.


## uri templates
The User-Agent MUST replace every occurrence of the template parameters with a value before issuing a request for the resource.  See URI Templates [http://tools.ietf.org/html/rfc6570](http://tools.ietf.org/html/rfc6570)

`application` – (OPTIONAL) Query parameter provides the server with the ability to filter the list of context enquiry links by the supplied Application or Version

`field` – (OPTIONAL) Query parameter provides the server with the ability to filter the list of context enquiry links by the supplied field


## example
An atom representation of a link to the context enquiry list resource
<pre>
&lt;link rel="http://www.temenos.com/rels/contextenquiry" type="application/atom+xml;type=entry" title="contextenquiry" href="ContextEnquiry{&application*}{&field*}"/&gt;
</pre>

The basic structure of the http request is as follows:
<pre>
GET /t24/ContextEnquiry?field=Customer&field=Currency HTTP/1.1
</pre>