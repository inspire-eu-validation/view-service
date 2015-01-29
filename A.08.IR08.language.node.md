# A.08.IR08.language.node

**Purpose**: Scenario 2: INSPIRE metadata are mapped to WMS capabilities elements to its full extent. It is mandatory to use the mapping provided in this Technical Guideline (described in Section 4.2.3.3.1.1 to 4.2.3.3.1.16. INSPIRE metadata elements that cannot be mapped to available ISO 19128 – WMS1.3.0 elements are implemented as Extended Capabilities. Metadata are published through a service's capabilities document and can be harvested by an INSPIRE Discovery service.

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
