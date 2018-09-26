# Supported languages node
 
**Purpose**: Regardless of the scenario chosen to be implemented, a language section shall be added in the extended capability of the service to fulfill the language requirements of the Network Services Regulation [INS NS]

**Prerequisites**

* [Schema validation](./schema-validation.md)
* [Extended Capabilities](./extended-capabilities.md)

**Test method**

* Check if there is a [SupportedLanguages](#SupportedLanguages) node.
* This list shall contain one or more [SupporterLanguage](#SupportedLanguage) nodes.

**Reference(s)**:

* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.1, Requirement 66

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
SupportedLanguages <a name="SupportedLanguages"></a>   | ./wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:SupportedLanguages
SupportedLanguage <a name="SupportedLanguage"></a>   | ./wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:SupportedLanguages/inspire_common:SupportedLanguage
