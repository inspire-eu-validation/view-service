# Category Layers

**Purpose**: A containing Category Layer itself includes a Name by which a map
portraying all of the nested layers can be requested at once.

**Prerequisites**

* Test for the existence of default element namespace.
* Test for the existence of the namespaces for INSPIRE View Services inspire_vs and inspire_common.

**Test method**

* Check whether the Capabilities section of a GetCapabilities response includes [Layer elements that have other Layer elements as children](#Layer).
* If yes, check whether the [Group Layer](#GroupLayer) contains a [Name](#Name) element.

**Reference(s)**:
* [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.3.4.11, IR 49

**Test type**: Automated

**Notes**

The second part of the requirement, stating that "If a metadata description of this category
composition exists then the MetadataURL for the Category Layer shall be provided." is covered by test case [coupled.resource.node](A.10.IR13.coupled.resource.node).


## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
Layer <a name="Layer"></a>   | /wms:WMS_Capabilities/wms:Capability/wms:Layer/wms:Layer
Group Layer <a name="GroupLayer"></a>   | /wms:WMS_Capabilities/wms:Capability/wms:Layer
Name <a name="Name"></a>   | /wms:WMS_Capabilities/wms:Capability/wms:Layer/wms:Name
