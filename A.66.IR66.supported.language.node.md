# A.66.IR66.supported.language.node

**Purpose**: A network service metadata response shall contain a list of the natural languages supported by the service. This list shall contain one or more languages that are supported.

**Prerequisites**

* Test for the existence of default element namespace.
* Test for the existence of the namespaces for INSPIRE View Services inspire_vs and inspire_common.

**Test method**

* Check if there is a supportedLanguages node in the ExtendedCapabilities section.

**Reference(s)**: 
* [TG VS](README.md#ref_TG_VS), Chapter 4.3.1
* IR Annex III, Part A, Chapter 2.2.3

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
SupportedLanguages <a name="SupportedLanguages"></a>   | /WMS_Capabilities/Capability/inspire_vs:ExtendedCapabilities/inspire_common:SupportedLanguages
ResponseLanguage <a name="ResponseLanguage"></a>   | /WMS_Capabilities/Capability/inspire_vs:ExtendedCapabilities/inspire_common:ResponseLanguage
ExtendedCapabilities <a name="ExtendedCapabilities"></a>   | /WMS_Capabilities/Capability/inspire_vs:ExtendedCapabilities
