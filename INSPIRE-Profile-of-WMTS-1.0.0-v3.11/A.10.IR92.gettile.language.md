# A.10.IR92.gettile.language

**Purpose**: The GetTile operation must support all languages declared in the GetCapabilities

**Prerequisites**

* WMTS generic operation tests and GetTile specific operation tests in the OGC WMTS ATS have been passed.
* Test for the schema validity of the ServiceMetadata document has been passed.
* Test for the existence and validity of the INSPIRE [ExtendedCapabilities](#extendedCapabilities) in ServiceMetadata document has been passed (*TODO: replace with a reference to this test after it's been created*).

**Test method**

The supported languages are not layer specific, so it's sufficient to the test with just any one layer. Also the it's
practically impossible to automatically verify that the returned tile images are provided in the requested language, so
the test just checks that the service accepts all the supported languages as request parameters, returning a non-empty
response.

* For each of the [SupportedLanguages](#supportedLanguages) as `language`:
  * Create a GetTile operation for the first layer listed in the capabilities document using the maximum allowed bounding box, either "image/png" or "image/gif" format (depending on which is supported), and the `language` as the value of the LANGUAGE request parameter.
  * Verify that an image in the requested image format is returned with HTTP status code 200.

**Reference(s)**: [TG VS](README.md#ref_TG_VS), chapter 5.2.4.1

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
ExtendedCapabilities <a name="extendedCapabilities"></a>   | /wmts:Capabilities/ows:OperationsMetadata/inspire_vs:ExtendedCapabilities
SupportedLanguages <a name="supportedLanguages"></a>   | /wmts:Capabilities/ows:OperationsMetadata/inspire_vs:ExtendedCapabilities/inspire_common:SupportedLanguages/inspire_common:SupportedLanguage
