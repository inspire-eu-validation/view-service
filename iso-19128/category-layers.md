# Category layers

**Purpose**: A containing Category Layer itself includes a Name by which a map
portraying all of the nested layers can be requested at once.

**Prerequisites**

* [Schema validation](./schema-validation.md)

**Test method**

* Check whether the Capabilities section of a GetCapabilities response includes [Layer elements that have other Layer elements as children](#Layer).
* If yes, check whether the [Group Layer](#GroupLayer) contains a [Name](#Name) element.

**Reference(s)**:

* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.4.11,  Requirement 49

**Test type**: Automated

**Notes**

The second part of the requirement, stating that "If a metadata description of this category composition exists then the MetadataURL for the Category Layer shall be provided." is covered by test case [Map Coupled Resource metadata](./map-coupled-resource-metadata.md).

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Layer <a name="Layer"></a>   | ./wms:Capability/wms:Layer/wms:Layer
Group Layer <a name="GroupLayer"></a>   | ./wms:Capability/wms:Layer
Name <a name="Name"></a>   | ./wms:Capability/wms:Layer/wms:Name
