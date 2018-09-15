# Supported and response languages node
 
**Purpose**: Regardless of the scenario chosen to be implemented, a language
section shall be added in the extended capability of the service to fulfil the language requirements of
the Network Services Regulation [INS NS]

**Prerequisites**

* [Schema validation](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/schema-validation)
* [Extended Capabilities](http://inspire.ec.europa.eu/id/ats/view-service/3.11/ISO-19128/extended-capabilities)

**Test method**

* Check if there is a [SupportedLanguages](#SupportedLanguages) node and a [ResponseLanguage](ResponseLanguage) node.

**Reference(s)**:

* [TG VS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/README#ref_TG_VS), Chapter 4.2.3.3.1, Requirement 66

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/README#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
SupportedLanguage <a name="SupportedLanguage"></a>   | ./wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:SupportedLanguages
ResponseLanguage <a name="ResponseLanguage"></a>   | ./wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:ResponseLanguage
