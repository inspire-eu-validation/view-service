# Select Select language capabilities

**Purpose**: The user must be able to select one of the supported languages. This language selection must be reflected in the provided capabilities document.

**Prerequisites**

* [Layer language](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/layer-language)

**Test method**

* Let the value of [GetCapabilities OnlineResource](#getcap-href) be ```getcapabilities-url```.
* For each [SupportedLanguage codes](#supported-languages) as ```lang-code```:
  * Create a GetCapabilities HTTP request by adding the parameters ```SERVICE=WMS``` (ISO 19128) or ```SERVICE=WMTS``` (for WMTS 1.0.0), ```REQUEST=GetCapabilities```, ```ACCEPTVERSIONS=1.3.0``` (for ISO 19128) or ```ACCEPTVERSIONS=1.0.0``` (for WMTS 1.0.0) and ```LANGUAGE=``` + ```lang-code``` to the ```getcapabilities-url```
  * Execute the request. If the returned resource can be parsed as a well-formed XML document and if the document passes tests [Schema validation](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/schema-validation) and [layer-language](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/layer-language):
    * Check that the [ResponseLanguage](#response-language) equals the ```lang-code```. If it does not, fail the test for this language.
  * Otherwise fail the test.
* If the test for any of the languages failed, fail the test. Otherwise pass the test.

**Reference(s)**:

* [TG VS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/README#ref_TG_VS), chapter 4.3.1
* [TG VS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/README#ref_TG_VS), chapter 5.2.3.3.3

**Test type**

Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/README#namespaces).

Abbreviation                                     |  XPath expression												|  Parameter  value
------------------------------------------------ | ---------------------------------------------------------------	| ---------------------------------------------------------------
GetCapabilities OnlineResource <a name="getcap-href"></a> | /wms:WMS_Capabilities/wms:Capability/wms:Request/wms:GetCapabilities/wms:DCPType/wms:HTTP/(wms:Get&#124;wms:Post)[1]/wms:OnlineResource/@xlink:href | ISO 19128
                                                          |  /wmts:Capabilities/ows:OperationsMetadata/ows:Operation[@name='GetCapabilities']/ows:DCP/ows:HTTP/ows:Get[ows:Constraint[@name='GetEncoding']/ows:AllowedValues/ows:Value='KVP']/@xlink:href
ExtendedCapabilities <a name="ExtendedCapabilities"></a>   | /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities | ISO 19128
                                                           | /wmts:Capabilities/ows:OperationsMetadata/inspire_vs_ows11:ExtendedCapabilities | WMTS 1.0.0
SupportedLanguage <a name="SupportedLanguage"></a>   | /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:SupportedLanguages/inspire_common:SupportedLanguage/inspire_common:Language | ISO 19128
                                                           | /wmts:Capabilities/ows:OperationsMetadata/inspire_vs_ows11:ExtendedCapabilities/inspire_common:SupportedLanguages/inspire_common:SupportedLanguage/inspire_common:Language | WMTS 1.0.0
ResponseLanguage <a name="ResponseLanguage"></a>   | /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:ResponseLanguage/inspire_common:Language | ISO 19128
                                                           | /wmts:Capabilities/ows:OperationsMetadata/inspire_vs_ows11:ExtendedCapabilities/inspire_common:ResponseLanguage/inspire_common:Language | WMTS 1.0.0
