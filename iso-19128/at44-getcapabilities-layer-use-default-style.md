# Layer Use Default Style

**Purpose**: Test that if empty style parameter is specified in the getMap request, default style is used in layer rendering.

**Prerequisites**

**Test method**

* Send a getMap request to the service endpoint with an empty STYLE parameter. In the respone:

  * Check if the style used in the response is the default style defined for the requested layer.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.4.8, Requirement 44

**Test type**: Manual

**Notes**

It is not possible to check automatically the styling used in the image of the response.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------

