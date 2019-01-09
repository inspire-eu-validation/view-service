# Common Request Parameters

**Purpose**: Test that common request parameters are implemented for the View Service operations. The common request parameters are: SERVICE, REQUEST and LANGUAGE.

**Prerequisites**

**Test method**

* Check that GetCapabilities operation implements the common request parameters. For that:

  * Send a request to the service endpoint with the following mandatory parameters and fixed values: SERVICE=WMTS, REQUEST=GetCapabilities

    * Check if a valid response is obtained.

  * Send a request to the service endpoint with the following mandatory parameters and fixed values: SERVICE=WMTS

    * Check if an exception is obtained.

  * Send a request to the service endpoint with the following mandatory parameters and fixed values: REQUEST=GetCapabilities

    * Check if an exception is obtained.

  * Send a request to the service endpoint with the following mandatory parameters and fixed values: SERVICE=WMTS, REQUEST=wrong

    * Check if an exception is obtained.

  * Send a request to the service endpoint with the following mandatory parameters and fixed values: SERVICE=wrong, REQUEST=GetCapabilities

    * Check if an exception is obtained.

  * For each supported language:

    * Send a request to the service endpoint with the following mandatory parameters and fixed values: SERVICE=WMTS, REQUEST=GetCapabilities, LANGUAGE=supported_lang

      * Check if a valid response is obtained and the response language is the same as requested.

* Check that GetTile operation implements the common request parameters. All the other parameters that are not common are filled with values obtained from the getCapabilities response. For that:

  * Send a request to the service endpoint with the following mandatory parameters and fixed values: SERVICE=WMTS, REQUEST=GetTile

    * Check if a valid response is obtained.

  * Send a request to the service endpoint with the following mandatory parameters and fixed values: SERVICE=WMTS

    * Check if an exception is obtained.

  * Send a request to the service endpoint with the following mandatory parameters and fixed values: REQUEST=GetTile

    * Check if an exception is obtained.

  * Send a request to the service endpoint with the following mandatory parameters and fixed values: SERVICE=WMTS, REQUEST=wrong

    * Check if an exception is obtained.

  * Send a request to the service endpoint with the following mandatory parameters and fixed values: SERVICE=wrong, REQUEST=GetTile

    * Check if an exception is obtained.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 5.2.1, Requirement 77

**Test type**: Automated/Manual

**Notes**

The language parameter is not mandatory in the request, but the service shall implement such option and be able to handle this parameter.

GetTile request has been automated only in the cases when the InspireCRS84Quad TileMatrixSet is implemented. The use of this TileMatrixSet is an INSPIRE Technical Guide recommendation. If this TileMatrixset is not implemented, the GetTile request common parameters implementation needs to be tested manually.

The GetTile response is an image so it cannot be checked automatically if the response is provided in the requested language.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------