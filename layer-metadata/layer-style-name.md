# Layer style name

**Purpose**: Each layer must include at least one style according to the both the ISO 19128 and WMTS specification. To be easily identifiable each style must include a human-readable name and a unique identifier for that style to be used in requests.

**Prerequisites**

* [Schema validation](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/schema-validation)

**Test method**

For each [Layer element](#Layer) provided by the service according to it's Service Metadata:
* For each [Style element](#Style) of the layer:
  * Check that the [Title element](#Title) exists and is a non-empty character string.
* Check that the character strings of the [Identifier elements](#Identifier) for each [Style elements](#Style) are unique within the style.

**Reference(s)**:
* [TG VS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/README#ref_TG_VS) 4.2.3.3.4.8, Requirement 41
* [TG VS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/README#ref_TG_VS) 4.2.3.3.4.8, Requirement 46
* [TG VS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/README#ref_TG_VS) 5.2.3.3.4.8, Requirement 90

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/README#namespaces).

Abbreviation                                     |  XPath expression												|  Parameter  value
------------------------------------------------ | ---------------------------------------------------------------	| ---------------------------------------------------------------
Layer <a name="Layer"></a> | /wms:WMS_Capabilities/wms:Capability/wms:Layer | ISO 19128
						   | /wmts:Capabilities/wmts:Contents/wmts:Layer | WMTS 1.0.0
Style <a name="Style"></a> | /wms:WMS_Capabilities/wms:Capability/wms:Layer/wms:Style | ISO 19128
						   | /wmts:Capabilities/wmts:Contents/wmts:Layer/wmts:Style | WMTS 1.0.0
Title <a name="Title"></a> | /wms:WMS_Capabilities/wms:Capability/wms:Layer/wms:Style/wms:Title | ISO 19128
						   | /wmts:Capabilities/wmts:Contents/wmts:Layer/wmts:Style/ows:Title | WMTS 1.0.0
Identifier <a name="Identifier"></a> | /wms:WMS_Capabilities/wms:Capability/wms:Layer/wms:Style/wms:Name | ISO 19128
							   		 | /wmts:Capabilities/wmts:Contents/wmts:Layer/wmts:Style/ows:Identifier | WMTS 1.0.0
