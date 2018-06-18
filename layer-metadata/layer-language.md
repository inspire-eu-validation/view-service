# Layer language

**Purpose**: The layer must be described in a language and terms the users are expected to understand.

**Prerequisites**

* [Schema validation](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/schema-validation)

**Test method**

For each [Layer element](#Layer) provided by the service according to it's Service Metadata:

* Check that the [Abstract element](#Abstract) is a non-empty character string. If so, pass the test.

**Reference(s)**:

* [TG VS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/README#ref_TG_VS), Chapter 4.2.3.3.4.2, Requirement 34
* [TG VS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/README#ref_TG_VS), Chapter 5.2.3.3.4.2, Requirement 86

**Test type**: Automated

**Notes**

This a the description of the layer (a portrayal), not the same thing as the metadata record of the dataset which the layer is visualising.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/README#namespaces).

Abbreviation                                     |  XPath expression												|  Parameter  value
------------------------------------------------ | ---------------------------------------------------------------	| ---------------------------------------------------------------
Layer <a name="Layer"></a> | /wms:WMS_Capabilities/wms:Capability/wms:Layer | ISO 19128
						   | /wmts:Capabilities/wmts:Contents/wmts:Layer | WMTS 1.0.0
Abstract <a name="Abstract"></a> | /wms:WMS_Capabilities/wms:Capability/wms:Layer/wms:Abstract | ISO 19128
								 | /wmts:Capabilities/wmts:Contents/wmts:Layer/ows:Abstract | WMTS 1.0.0
