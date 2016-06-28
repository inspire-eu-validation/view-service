# Language selection capabilities

**Purpose**: The user must be able to select one of the supported languages.
This language selection must be reflected in the provided capabilities document.

**Prerequisites**

* [Schema validation](schema-validation.md)
* [Check supported and response languages node](check-supported-and-response-languages-node.md)

**Test method**

* Let the value of [GetCapabilities OnlineResource](#getcap-href) be ```getcapabilities-url```.
* For each [SupportedLanguage codes](#supported-languages) as ```lang-code```:
  * Create a GetCapabilities HTTP request by adding the parameters ```SERVICE=WMS```, ```REQUEST=GetCapabilities```, ```VERSION=1.3.0``` and ```LANGUAGE=``` + ```lang-code``` to the ```getcapabilities-url```
  * Execute the request. If the returned resource can be parsed as a valid XML document and if the document passes tests [Schema validation](schema-validation.md) and [check supported and response languages node](check-supported-and-response-languages-node.md):
    * Check that the [ResponseLanguage code](#response-language) equals the ```lang-code```. If it does not, fail the test for this language.
  * Otherwise fail the test.
* If the test for any of the languages failed, fail the test. Otherwise pass the test.

**Reference(s)**:

* [TG VS](README.md#ref_TG_VS), chapter 4.3.1
* [TG MD](README.md#ref_TG_MD), chapter 2.2.7

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
SupportedLanguage codes <a name="supported-languages"></a>   | /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities[1]/inspire_common:SupportedLanguages/inspire_common:SupportedLanguage/inspire_common:Language
ResponseLanguage code <a name="response-language"></a>   | /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities[1]/inspire_common:ResponseLanguage/inspire_common:Language
GetCapabilities OnlineResource <a name="getcap-href"></a> | /wms:WMS_Capabilities/wms:Capability/wms:Request/wms:GetCapabilities/wms:DCPType/wms:HTTP/(wms:Get&#124;wms:Post)[1]/wms:OnlineResource/@xlink:href
