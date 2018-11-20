# Layer Default Style

**Purpose**: Test that a style is provided with the name of the default style defined in the INSPIRE Data Specification for the theme of the layer.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * For each Layer element:

    If the INSPIRE Data Specification defines a default style for the harmonised layer,

      * Check that the [Name](#name1) of one of the Style elements provided for the layer is equal to the name of the default style defined in the Data Specification.

    If it is not defined a default style for that harmonised layer name in the Theme INSPIRE Data Specification, the test passes.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.4.8, Requirement 42

**Test type**: Automated

**Notes**

The multiplicity of this element is 1.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Name <a name="name1"></a> | wms:Capability/wms:Layer/wms:Style/wms:Name
