# Layer title

**Purpose**: Layer title is mapped with the corresponding Title element in the Capabilities. The harmonised title of a layer for an INSPIRE spatial data theme is defined by INS DS and shall be subject to multilingualism (translations shall appear in each mono-lingual capabilities localised documents).

**Prerequisites**

* [Schema validation](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/schema-validation)

**Test method**

For each [Layer element](#Layer) provided by the service according to it's Service Metadata:

* Check that the [Title element](#Title) is a non-empty character string. If so, pass the test.

**Reference(s)**:

* [TG VS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/README#ref_TG_VS), Chapter 4.2.3.3.4.1, Requirement 33
* [TG VS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/README#ref_TG_VS), Chapter 5.2.3.3.4.1, Requirement 85

**Test type**

Automated

**Notes**

The validation of the correctness of the translated title is not done due to it's complexity and the controversy over the usefulness of the harmonised layer titles. If this is decided to be necessary, the procedure should be similar to one used in `A.04.layer.name.id`.

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/README#namespaces).

Abbreviation                                     |  XPath expression												|  Parameter  value
------------------------------------------------ | ---------------------------------------------------------------	| ---------------------------------------------------------------
Title <a name="Title"></a> | /wms:WMS_Capabilities/wms:Capability/wms:Layer/wms:Title | ISO 19128
						   | /wmts:Capabilities/wmts:Contents/wmts:Layer/ows:Title  | WMTS 1.0.0
Layer <a name="Layer"></a> | /wms:WMS_Capabilities/wms:Capability/wms:Layer | ISO 19128
						   | /wmts:Capabilities/wmts:Contents/wmts:Layer | WMTS 1.0.0

