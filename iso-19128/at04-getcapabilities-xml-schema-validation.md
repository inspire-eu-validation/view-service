
# XML schema validation

**Purpose**: Test that the XML capabilities document is schema valid.

**Prerequisites**

**Test method**
* Send a GetCapabilities request.

    * Validate document against XML schema located in http://schemas.opengis.net/wms/1.3.0/.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.1, Requirement 4

**Test type**: Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
