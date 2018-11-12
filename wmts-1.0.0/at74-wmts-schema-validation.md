
# WMTS XML schema validation

**Purpose**: Test that the XML capabilities document is WMTS schema valid.

**Prerequisites**

**Test method**
* Send a GetCapabilities request.

    * Validate document against XML schema located in http://schemas.opengis.net/wmts/1.0/.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 5.1, Requirement 74

**Test type**: Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
