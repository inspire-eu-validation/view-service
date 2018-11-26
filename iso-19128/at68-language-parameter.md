# Language Parameter

**Purpose**:

Test that the service accepts the parameter LANGUAGE to request the capabilities document in an specific language.

**Prerequisites**

**Test method**

* Send a GetCapabilities request without LANGUAGE parameter.

    * Check that [Default Language](#defaultLanguage) is accordance with ISO 639-2/B alpha 3.

* Send a GetCapabilities request with LANGUAGE parameter and value same as [Default Language](#defaultLanguage).

    * Check that [Title](#title) and [Abstract](#abstract) elements are the same as default ones.


**Reference(s)**:

* [TG VS](./README.md#ref_TG_VS), requirement 68

**Test type**: Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Default Language <a name="defaultLanguage"></a> | inspire_common:SupportedLanguages/inspire_common:DefaultLanguage/inspire_common:Language
Title <a name="title"></a> | /wms:WMS_Capabilities/Service/Title
Abstract <a name="abstract"></a> | /wms:WMS_Capabilities/Service/Abstract