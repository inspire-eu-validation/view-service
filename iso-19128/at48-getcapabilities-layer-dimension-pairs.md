# Layer Dimension Pairs

**Purpose**: Test that is provided a Dimension element to declare one or more dimensional parameters.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * For each [Layer](#layer) element:

    * Check if exists a [Dimension](#dimension) element. If yes, for each Dimension

      * Check that the element has an attribute [Dimension Name](#dimensionName) defining the name of the dimension and [Dimension Units](#dimensionUnits) attributes defining the units of the measure. 

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.4.10, Requirement 48

**Test type**: Automated

**Notes**

The multiplicity of this element is 0 or more.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Layer <a name="layer"></a> | wms:Capability/*/wms:Layer
Dimension <a name="dimension"></a> | wms:Capability/*/wms:Layer/wms:Dimension
Name <a name="dimensionName"></a> | wms:Capability/*/wms:Layer/wms:Dimension/@name
Units <a name="dimensionUnits"></a> | wms:Capability/*/wms:Layer/wms:Dimension/@units
