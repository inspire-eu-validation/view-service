# Language Supported

**Purpose**:

Test that the capabilities document contains the language elements with the correct multiplicity.

**Prerequisites**

**Test method**

* Send a GetCapabilities request

    * Check if it exists exactly one [Supported Languages](#supportedLanguages) node.

    * Check if it exists exactly one [Default Language](#defaultLanguage) node and its value is not empty.

    * Check if it exists zero or more [Supported Language](#supportedLanguage) node and the value of every supported language is not empty.

    * Check if it exists exactly one [Response Language](#responseLanguage) node and its value is not empty.

* If any of the checks fails, the test fails

**Reference(s)**:

* [TG VS](./README.md#ref_TG_VS), requirement 71

**Test type**: Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Supported Languages <a name="supportedLanguages"></a> | inspire_common:SupportedLanguages
Default Language <a name="defaultLanguage"></a> | inspire_common:SupportedLanguages/inspire_common:DefaultLanguage/inspire_common:Language
Supported Language <a name="supportedLanguage"></a> | inspire_common:SupportedLanguages/inspire_common:SupportedLanguage/inspire_common:Language
Response Language <a name="responseLanguage"></a> | inspire_common:ResponseLanguage/inspire_common:Language