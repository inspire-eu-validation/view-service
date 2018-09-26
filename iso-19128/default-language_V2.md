# Default language

**Purpose**: The default language for the service must be provided in order the user to be able to know which language can be expected to be used if the capabilities document when no language is explicitly requested. The client preferred language shall by provide as the 'LANGUAGE' parameter in the GetCapabilities HTTP request.

**Prerequisites**

* [Schema validation](./schema-validation.md)
* [Supported and response languages node](./supported-and-response-languages-node.md)

**Test method**


* The client preferred language may be specified in the GetCapabilities HTTP request adding the LANGUAGE parameter.
  * The LANGUAGE parameter values ar based on [ISO 639-2/B alpha 3 codes]
  * The GetCapabilities HTTP request structure, to the [GetCapabilitiesOnlineResource](#getcap-href), would include the parameters SERVICE=WMS, REQUEST=GetCapabilities, VERSION=1.3.0 and LANGUAGE=[<ISO 639-2/B alpha 3 code>](https://www.loc.gov/standards/iso639-2/php/code_list.php)
* If the requested language parameter value is contained in the SupportedLanguages list, the natural language fields shall be in the requested language.
* If not (it is unsupported language or it is absent), the fields relative to Titles and Abstracts shall be provided in the [default service language](#default-language).


**Reference(s)**:

* [TG VS](./README.md#ref_TG_VS), chapter 4.3.1, Requirement 68, 69
* [lang-code ISO 639-2](https://www.loc.gov/standards/iso639-2/php/code_list.php)

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
GetCapabilities OnlineResource <a name="getcap-href"></a> | /wms:WMS_Capabilities/wms:Capability/wms:Request/wms:GetCapabilities/wms:DCPType/wms:HTTP/(wms:Get&#124;wms:Post)[1]/wms:OnlineResource/@xlink:href
DefaultLanguage <a name="default-language"></a>   | ./wms:Capability/inspire_vs:ExtendedCapabilities[1]/inspire_common:SupportedLanguages/inspire_common:DefaultLanguage/inspire_common:Language