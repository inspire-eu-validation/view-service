# schema.valid

**Purpose**: The operation for implementing INSPIRE Get View Service Metadata operation is the GetCapabilities operation. The parameters defined within the ISO 19128 / WMTS 1.0.0 standard shall be used to convey relevant information in order to get the expected responses as described in INS NS, Annex III, Section 2.2 of the Regulation on INSPIRE Network Services.

**Prerequisites**

**Test method**

* For ISO 19128: Check, if the [INSPIRE View Service 1.0 schema](http://inspire.ec.europa.eu/schemas/inspire_vs/1.0/inspire_vs.xsd) is referenced in the service capabilities. Then check that the GetCapabilities request result validates against this schema.
* For WMTS 1.0.0: Check, if the [INSPIRE View Service 1.0 schema](http://inspire.ec.europa.eu/schemas/inspire_vs_ows11/1.0/inspire_vs_ows_11.xsd) is referenced in the service capabilities. Then check that the GetCapabilities request result validates against this schema plus the [WMTS 1.0.0 schema](http://schemas.opengis.net/wmts/1.0/wmtsGetCapabilities_response.xsd).

**Reference (s)**: 

* [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.2
* [TG VS](README.md#ref_TG_VS), Chapter 5.2.3.3.1

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                     |  XPath expression												|  Parameter  value
------------------------------------------------ | ---------------------------------------------------------------	| ---------------------------------------------------------------
service Capabilities <a name="service Capabilities"></a>   | /wms:WMS_Capabilities/@xsi:schemaLocation | ISO 19128
                                                           | /wmts:Capabilities/@xsi:schemaLocation | WMTS 1.0.0
