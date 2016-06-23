# A.06.IR08.language.node

**Purpose**: Regardless of the scenario chosen to be implemented, a language
section shall be added in the extended capability of the service to fulfil the language requirements of
the Network Services Regulation [INS NS]

**Prerequisites**

* Test for the existence of default element namespace.
* Test for the existence of the namespaces for INSPIRE View Services inspire_vs and inspire_common.

**Test method**

* Check if there is a supportedLanguages node and a ResponseLanguage node in the ExtendedCapabilities section.

**Reference(s)**:
* [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.3.1
* IR Annex III, Part A, Chapter 2.2.3

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
SupportedLanguage <a name="SupportedLanguage"></a>   | /WMS_Capabilities/Capability/inspire_vs:ExtendedCapabilities/inspire_common:SupportedLanguages
ResponseLanguage <a name="ResponseLanguage"></a>   | /WMS_Capabilities/Capability/inspire_vs:ExtendedCapabilities/inspire_common:ResponseLanguage
ExtendedCapabilities <a name="ExtendedCapabilities"></a>   | /WMS_Capabilities/Capability/inspire_vs:ExtendedCapabilities
