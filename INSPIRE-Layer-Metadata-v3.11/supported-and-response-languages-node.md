# Supported and response languages node

**Purpose**: A language section shall be added in the extended capabilities of the service to fulfil the language requirements of the Network Services Regulation [INS NS]

**Prerequisites**

* [Extended Capabilities](extended-capabilities.md)

**Test method**

* Check if there is a [SupportedLanguages](#SupportedLanguages) node and a [ResponseLanguage](ResponseLanguage) node.

**Reference(s)**:

* [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.3.1
* [TG VS](README.md#ref_TG_VS), Chapter 5.2.3.3.1
* [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.1

**Test type**:Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                     |  XPath expression												|  Parameter  value
------------------------------------------------ | ---------------------------------------------------------------	| ---------------------------------------------------------------
ExtendedCapabilities <a name="ExtendedCapabilities"></a>   | /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities | ISO 19128
                                                           | /wmts:Capabilities/ows:OperationsMetadata/inspire_vs_ows11:ExtendedCapabilities | WMTS 1.0.0
SupportedLanguage <a name="SupportedLanguage"></a>   | /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:SupportedLanguages | ISO 19128
                                                           | /wmts:Capabilities/ows:OperationsMetadata/inspire_vs_ows11:ExtendedCapabilities/inspire_common:SupportedLanguages | WMTS 1.0.0
ResponseLanguage <a name="ResponseLanguage"></a>   | /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:ResponseLanguage | ISO 19128
                                                           | /wmts:Capabilities/ows:OperationsMetadata/inspire_vs_ows11:ExtendedCapabilities/inspire_common:ResponseLanguage | WMTS 1.0.0
