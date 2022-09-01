# Harmonised Layer Name

**Purpose**: Test that at least a harmonised layer according to [IR IOP](./README.md#ref_IR_IOP) is present, which layer name shall comply with the harmonised layer name defined in Article 14 of [IR IOP](./README.md#ref_IR_IOP).

**Prerequisites**: The WMS is related to a harmonized dataset (to be manually checked).

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * Check that at least a [Layer](#layer) element with the value of the [Layer Name](#layerName) element that matches one of the harmonised layer names given in [IR IOP](./README.md#ref_IR_IOP) or its amendments, is present.

  * If no layers are found, report a warning message indicating that if the WMS under test is related to a harmonized dataset at least a harmonised layer according to [IR IOP](./README.md#ref_IR_IOP) shall be present.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.4.6, Requirement 39 bis
* [IR IOP](./README.md#ref_IR_IOP), Article 14

**Test type**: Automated

**Notes**

A view service may contain one or more harmonised and/or one or more non-harmonised layers.

The multiplicity of this element is 1 for each named Layer.

A Layer that contains a Named child element is a 'named Layer'.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Layer <a name="layer"></a> | wms:Capability/*/wms:Layer
Layer Name <a name="layerName"></a> | wms:Capability/*/wms:Layer/wms:Name
