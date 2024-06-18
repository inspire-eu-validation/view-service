# Language Response

**Purpose**:

Test that the service Language Response changes according with the request.

**Prerequisites**

**Test method**

This test only applies to [Scenario 1 and 2](./README.md#scenarios). Otherwise, a manual check is required.

Automatic test:

* Send a GetCapabilities request without LANGUAGE parameter.

    * Check that the [Response Language](#responseLanguage) is the same as the [Default Language](#defaultLanguage).

* Send a GetCapabilities request with an invalid LANGUAGE parameter.

    * Check that the [Response Language](#responseLanguage) is the same as the [Default Language](#defaultLanguage).

* For each [Supported Language](#supportedLanguage),

    * Check that [Supported Language](#supportedLanguage) is accordance with ISO 639-2/B alpha 3.

    * Send a GetCapabilities request with a supported language parameter.

        * Check that the [Response Language](#responseLanguage) is the same as the requested one.
     
Manual test:

* If the Extended Capabilities section, with information about the response/supported languages, is not provided it means that the default language of the service corresponds to the data set metadata default language. Check manually that the service's default language is the same as the data set metadata default language (gmd:MD_Metadata/gmd:language/gmd:LanguageCode).

**Reference(s)**:

* [TG VS](./README.md#ref_TG_VS), requirement 70

**Test type**: Automated + Manual

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Default Language <a name="defaultLanguage"></a> | inspire_common:SupportedLanguages/inspire_common:DefaultLanguage/inspire_common:Language
Supported Language <a name="supportedLanguage"></a> | inspire_common:SupportedLanguages/inspire_common:SupportedLanguage/inspire_common:Language
Response Language <a name="responseLanguage"></a> | inspire_common:ResponseLanguage/inspire_common:Language
