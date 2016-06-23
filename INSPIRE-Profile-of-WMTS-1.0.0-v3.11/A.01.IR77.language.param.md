# A.01.IR77.language.param

**Purpose**: The View Service must be able to return the service metadata document in all the languages advertised as supported.

**Prerequisites**

* Test for the schema validity of the ServiceMetadata document has been passed.
* Test for the existence and validity of the INSPIRE [ExtendedCapabilities](#extendedCapabilities) in ServiceMetadata document has been passed (*TODO: replace with a reference to this test after it's been created*).

**Test method**

For each [SupportedLanguages](#supportedLanguages) as `language`:
* Make a ServiceMetadata request for this service (RESTful or procedure oriented) using the `language` string as the value for LANGUAGE request parameter,
* Check that the value of the [ResponseLanguage](#responseLanguage) of each of the returned capabilities documents equals `language`.

**Reference(s)**: [TG VS](README.md#ref_TG_VS), Chapter 5.2.6

**Test type**: Automated

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
ExtendedCapabilities <a name="extendedCapabilities"></a>   | /wmts:Capabilities/ows:OperationsMetadata/inspire_vs:ExtendedCapabilities
SupportedLanguages <a name="supportedLanguages"></a>   | /wmts:Capabilities/ows:OperationsMetadata/inspire_vs:ExtendedCapabilities/inspire_common:SupportedLanguages/inspire_common:SupportedLanguage
ResponseLanguage <a name="responseLanguage"></a>   | /wmts:Capabilities/ows:OperationsMetadata/inspire_vs:ExtendedCapabilities/inspire_common:ResponseLanguage
