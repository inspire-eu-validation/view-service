# A.28.IR33.layer.title.node

**Purpose**: Layer title is mapped with wms:Title. The harmonised title of a layer for an INSPIRE spatial data theme is defined by INS DS and shall be subject to multilingualism (translations shall appear in each mono-lingual capabilities localised documents).

**Prerequisites**

* Test for the existence of default element namespace.

**Test method**

For each [Layer element](#Layer) provided by the service according to it's Service Metadata:

* Check that the [Title element](#Title) is a non-empty character string. If so, pass the test.

**Reference(s)**:
* [TG VS](../README.md#ref_TG_VS), Chapter 4.2.3.3.4.1, Requirement 33
* [TG VS](../README.md#ref_TG_VS), Chapter 5.2.3.3.4.1, Requirement 85

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                     |  XPath expression												|  Parameter  value
------------------------------------------------ | ---------------------------------------------------------------	| ---------------------------------------------------------------
Title <a name="Title"></a> | /wms:WMS_Capabilities/wms:Capability/wms:Layer/wms:Title | ISO 19128
						   | /wmts:Capabilities/wmts:Contents/wmts:Layer/ows:Title  | WMTS 1.0.0
Layer <a name="Layer"></a> | /wms:WMS_Capabilities/wms:Capability/wms:Layer | ISO 19128
						   | /wmts:Capabilities/wmts:Contents/wmts:Layer | WMTS 1.0.0

