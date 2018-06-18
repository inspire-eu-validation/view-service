# Category layers

**Purpose**: A containing Category Layer itself includes a Name by which a map
portraying all of the nested layers can be requested at once.

**Prerequisites**

* [Schema validation](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/schema-validation)

**Test method**

* Check whether the Capabilities section of a GetCapabilities response includes [Layer elements that have other Layer elements as children](#Layer).
* If yes, check whether the [Group Layer](#GroupLayer) contains a [Name](#Name) element.

**Reference(s)**:

* [TG VS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/README#ref_TG_VS), Chapter 4.2.3.3.4.11, Requirement 49

**Test type**: Automated

**Notes**

The second part of the requirement, stating that "If a metadata description of this category composition exists then the MetadataURL for the Category Layer shall be provided." is covered by test case [Map Coupled Resource metadata](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/map-coupled-resource-metadata).

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
Layer <a name="Layer"></a>   | /wms:WMS_Capabilities/wms:Capability/wms:Layer/wms:Layer
Group Layer <a name="GroupLayer"></a>   | /wms:WMS_Capabilities/wms:Capability/wms:Layer
Name <a name="Name"></a>   | /wms:WMS_Capabilities/wms:Capability/wms:Layer/wms:Name
