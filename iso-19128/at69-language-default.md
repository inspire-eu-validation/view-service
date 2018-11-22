# Language Default

**Purpose**:

Test that Titles and Abstracts are not affected when the LANGUAGE parameter is absent or unsupported.

**Prerequisites**

**Test method**

* Send a GetCapabilities request without LANGUAGE parameter.

* Send a GetCapabilities request with an invalid LANGUAGE parameter.

    * Check that [Title](#title) and [Abstract](#abstract) elements are the same as default ones.

**Reference(s)**:

* [TG VS](./README.md#ref_TG_VS), requirement 69

**Test type**: Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Default Language <a name="defaultLanguage"></a> | inspire_common:SupportedLanguages/inspire_common:DefaultLanguage/inspire_common:Language
Response Language <a name="responseLanguage"></a> | inspire_common:ResponseLanguage/inspire_common:Language
Title <a name="title"></a> | /wms:WMS_Capabilities/Service/Title
Abstract <a name="abstract"></a> | /wms:WMS_Capabilities/Service/Abstract