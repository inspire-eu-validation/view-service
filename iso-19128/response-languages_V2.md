# Response language

**Purpose**: The response language shall be included into Extended Capabilities. Depending on the requested language the value 

**Prerequisites**

* [Schema validation](./schema-validation.md)
* [Supported and response languages node](./supported-and-response-languages-node.md)

**Test method**

* Let the value of [GetCapabilities OnlineResource](#getcap-href) be ```getcapabilities-url```.
* Let the [default language code](#default-language) be ```lang-code```:
  * Create a GetCapabilities HTTP request by adding the parameters ```SERVICE=WMS```, ```REQUEST=GetCapabilities```, ```VERSION=1.3.0``` to the ```getcapabilities-url```.
  * Execute the request. If the returned resource can be parsed as a valid XML document and if the document passes tests [Schema validation](./schema-validation.md) and [supported and response languages node](./supported-and-response-languages-node.md):
    * Check that the [response language code](#response-language) equals the ```lang-code```.
    * In the response, the fields relative to Titles and Abstracts shall be provided in the ```lang-code``` language.
  

* Let ```unsupported-lang``` be a language code that is not included in the supported languages or is empty:
  * Create a GetCapabilities HTTP request by adding the parameters SERVICE=WMS, REQUEST=GetCapabilities, VERSION=1.3.0 and LANGUAGE=```unsupported-lang``` to the ```getcapabilities-url```. 
    * The language to be requested is included in the 'LANGUAGE' parameter of the request.
    * The LANGUAGE parameter values ar based on [ISO 639-2/B alpha 3 codes](https://www.loc.gov/standards/iso639-2/php/code_list.php).
  * Execute the request. If the returned resource can be parsed as a valid XML document and if the document passes tests [Schema validation](./schema-validation.md) and [supported and response languages node](./supported-and-response-languages-node):
    * Check that [response language](#response-language) correspond to the service [default language code](#default-language). If it does not, fail the test for this language.


**Reference(s)**:

* [TG VS](./README.md#ref_TG_VS), chapter 4.3.1, Requirement 68, 69, 70, 71 , 73
* [lang-code ISO 639-2](https://www.loc.gov/standards/iso639-2/php/code_list.php)

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
GetCapabilities OnlineResource <a name="getcap-href"></a> | /wms:WMS_Capabilities/wms:Capability/wms:Request/wms:GetCapabilities/wms:DCPType/wms:HTTP/(wms:Get&#124;wms:Post)[1]/wms:OnlineResource/@xlink:href
DefaultLanguage <a name="default-language"></a>   | ./wms:Capability/inspire_vs:ExtendedCapabilities[1]/inspire_common:SupportedLanguages/inspire_common:DefaultLanguage/inspire_common:Language
OnlineResource <a name="getcap-href"></a> | ./wms:Capability/wms:Request/wms:GetCapabilities/wms:DCPType/wms:HTTP/(wms:Get&#124;wms:Post)[1]/wms:OnlineResource/@xlink:href
ResponseLanguage <a name="response-language"></a>   | ./wms:Capability/inspire_vs:ExtendedCapabilities[1]/inspire_common:ResponseLanguage/inspire_common:Language
