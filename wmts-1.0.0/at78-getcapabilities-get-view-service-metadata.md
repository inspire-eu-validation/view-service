# Get View Service Metadata

**Purpose**: Test that the View Service metadata, Operations Metadata, Layers Metadata and Languages response parameters are contained in the Get View Service operation response. 

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * Check if [ServiceIdentification](#ServiceIdentification) and [ServiceProvider](#ServiceProvider) element is provided with the View Service Metadata.

  * Check if [OperationsMetadata](#OperationsMetadata) element is provided with the Operations Metadata.

  * Check if [Contents](#Contents) element is provided with the Layer Metadata.

  * Check if [SupportedLanguages](#SupportedLanguages) and [ResponseLanguage](#ResponseLanguage) elements are provided.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 5.2.3.1, Requirement 78

**Test type**: Automated

**Notes**

The multiplicity of these elements is 1.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
ServiceIdentification <a name="ServiceIdentification"></a> | ows:ServiceIdentification
ServiceProvider <a name="ServiceProvider"></a> | ows:ServiceProvider
OperationsMetadata <a name="OperationsMetadata"></a> | ows:OperationsMetadata
Contents <a name="Contents"></a> | Contents
SupportedLanguages <a name="SupportedLanguages"></a> | ows:OperationsMetadata/inspire_vs:ExtendedCapabilities/inspire_common:SupportedLanguages
ResponseLanguage <a name="ResponseLanguage"></a> | ows:OperationsMetadata/inspire_vs:ExtendedCapabilities/inspire_common:ResponseLanguage