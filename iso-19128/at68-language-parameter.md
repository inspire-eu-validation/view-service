# Language Parameter

**Purpose**:

Test that the service accepts the parameter LANGUAGE to request the capabilities document in an specific language.

**Prerequisites**

**Test method**

* Send a GetCapabilities request with parameter LANGUAGE and value same as [Default Language](#defaultLanguage).

    * Check that [Default Language](#defaultLanguage) is accordance with ISO 639-2/B alpha 3.

    * Check that the service accepts the LANGUAGE parameter and the [Response Language](#responseLanguage) is the same as the requested one.

    * Check that Titles and Abstracts fields are the same as default ones.


**Reference(s)**:

* [TG VS](./README.md#ref_TG_VS), requirement 68

**Test type**: Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Default Language <a name="defaultLanguage"></a> | inspire_common:SupportedLanguages/inspire_common:DefaultLanguage/inspire_common:Language
Response Language <a name="responseLanguage"></a> | inspire_common:ResponseLanguage/inspire_common:Language