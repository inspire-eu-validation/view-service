# Layer Style

**Purpose**: Test that if no style is specified in the getMap request, the inspire_common:DEFAULT style is used in layer rendering.

**Prerequisites**

**Test method**

* Send a getMap request to the service endpoint without the STYLE parameter. In the respone:

  * Check if the style used in the response is the inspire_common:DEFAULT.

**Reference(s)**
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.4.8, Requirement 44

**Test type**: Manual

**Notes**

It is not possible to check automatically the styling used in the image of the response.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------

