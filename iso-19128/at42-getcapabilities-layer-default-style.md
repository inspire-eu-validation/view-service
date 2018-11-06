# Layer Default Style

**Purpose**: Test that a inspire_common:DEFAULT style is given for each theme.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * For each wms:Layer element:

    * Check if it is provided at least a default style for each theme. Style unique identifier value must be inspire_common:DEFAULT.

**Reference(s)**
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.4.8, Requirement 42

**Test type**: Automated

**Notes**

The multiplicity of this element is 1.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Default Style <a name="defaultStyle"></a> | wms:Capability/wms:Layer/wms:Style/wms:Name
