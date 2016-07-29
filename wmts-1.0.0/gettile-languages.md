# GetTile language support

**Purpose**: The GetTile operation must support all languages declared in the GetCapabilities

**Prerequisites**

**Test method**

The supported languages are not layer specific, so it's sufficient to the test with just any one layer. Also the it's practically impossible to automatically verify that the returned tile images are provided in the requested language, so the test just checks that the service accepts all the supported languages as request parameters, returning a non-empty response.

* For each of the [supported languages](#supportedLanguages) as `language`:
  * Create a GetTile operation for the first layer listed in the capabilities document using the maximum allowed bounding box, either "image/png" or "image/gif" format (depending on which is supported), and the `language` as the value of the LANGUAGE request parameter.
  * Verify that an image in the requested image format is returned with HTTP status code 200.

**Reference(s)**: 

* [TG VS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/wmts-1.0.0/README#ref_TG_VS), Requirement 92

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/view-service/3.11/wmts-1.0.0/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
supported languages <a name="supportedLanguages"></a>   | /wmts:Capabilities/ows:OperationsMetadata/inspire_vs:ExtendedCapabilities/inspire_common:SupportedLanguages/inspire_common:SupportedLanguage
