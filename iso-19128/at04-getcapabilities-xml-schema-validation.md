
# XML schema validation

**Purpose**: Test that the XML capabilities document is schema valid.

**Prerequisites**

**Test method**
* Send a GetCapabilities request.

    * Check that one of the proper schema is declared in the _schemaLocation_ attribute, i.e. http://inspire.ec.europa.eu/schemas/inspire_vs/1.0/inspire_vs.xsd or http://schemas.opengis.net/wms/1.3.0/capabilities_1_3_0.xsd
    * Validate the document against XML schemas declared in the _schemaLocation_ attribute.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.1, Requirement 4

**Test type**: Automated

**Notes**

**Contextual XPath references**

The namespace prefixes are used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
