# Default language

**Purpose**: The default language for the service must be provided in order the user to be able to know which
language can be expected to be used if the capabilities document when no language is explicitly requested.

**Prerequisites**

* [Schema validation](Schema validation.md)
* [Check supported and response languages node](Check supported and response languages node.md)

**Test method**

* Let the value of [GetCapabilities OnlineResource](#getcap-href) be ```getcapabilities-url```.
* Let the [DefaultLanguage code](#default-language) be ```lang-code```.
* Create a GetCapabilities HTTP request by adding the parameters ```SERVICE=WMS```, ```REQUEST=GetCapabilities```, ```VERSION=1.3.0``` to the ```getcapabilities-url```.
* Execute the request. If the returned resource can be parsed as a valid XML document and if the document passes tests [Schema validation](Schema validation.md) and [Check supported and response languages node](Check supported and response languages node.md):
  * Check that the [ResponseLanguage code](#response-language) equals the ```lang-code```. If it does pass the test.
* Otherwise fail the test.

**Reference(s)**:

* [TG VS](README.md#ref_TG_VS), chapter 4.3.1
* [TG MD](README.md#ref_TG_MD), chapter 2.2.7

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
DefaultLanguage code <a name="default-language"></a>   | /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities[1]/inspire_common:SupportedLanguages/inspire_common:DefaultLanguage/inspire_common:Language
ResponseLanguage code <a name="response-language"></a>   | /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities[1]/inspire_common:ResponseLanguage/inspire_common:Language
GetCapabilities OnlineResource <a name="getcap-href"></a> | /wms:WMS_Capabilities/wms:Capability/wms:Request/wms:GetCapabilities/wms:DCPType/wms:HTTP/(wms:Get&#124;wms:Post)[1]/wms:OnlineResource/@xlink:href
