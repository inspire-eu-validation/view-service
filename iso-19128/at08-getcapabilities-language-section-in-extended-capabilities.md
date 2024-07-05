# Language section in Extended Capabilities

**Purpose**: Test that a language section is provided to fulfil the language requirements, if more than one language is supported.

**Prerequisites**

**Test method**

This test only applies to [Scenario 1 and 2](./README.md#scenarios). Otherwise, the test case is skipped.

* Send a getCapabilities request to the service endpoint. Into the response:

  * Check that there is a [SupportedLanguages](#SupportedLanguage) node and a [ResponseLanguage](#ResponseLanguage) node in the ExtendedCapabilities section.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.1, Requirement 8

**Test type**: Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
SupportedLanguage <a name="SupportedLanguage"></a>   | wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:SupportedLanguages
ResponseLanguage <a name="ResponseLanguage"></a>   | wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:ResponseLanguage
