# Layer Simple Style

**Purpose**: Test that the layers with no associated default style applies the style defined in the INSPIRE Generic Conceptual Model.

**Prerequisites**

**Test method**

* For each [Layer](#layer) element with no associated default style,
  
  * Check if the applied style match with:
    * Point: grey square, 6 pixels
    * Curve: black solid line, 1 pixel
    * Surface: black solid line, 1 pixel, grey fill

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.4.8, Requirement 43

**Test type**: Manual

**Notes**

This implementation cannot be automated due to the nature of its content.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Layer <a name="layer"></a> | wms:Capability/*/wms:Layer
