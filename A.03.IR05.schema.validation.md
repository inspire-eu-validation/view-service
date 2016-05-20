# A.03.IR05.schema.validation

**Purpose**: The operation for implementing INSPIRE Get View Service Metadata operation is the GetCapabilities operation. The parameters defined within the ISO 19128 standard shall be used to convey relevant information in order to get the expected responses as described in INS NS, Annex III, Section 2.2 of the Regulation on INSPIRE Network Services.

**Prerequisites**

* Test for the existence of default element namespace.

**Test method**

* First check if the [INSPIRE View Service 1.0 schema](http://inspire.ec.europa.eu/schemas/inspire_vs/1.0/inspire_vs.xsd) is given in the service capabilities
* Then check that the GetCapabilities request result validates against this schema.

**Reference (s)**: [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.2

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
service Capabilities <a name="service Capabilities"></a>   | /WMS_Capabilities/@xsi:schemaLocation
GetCapabilities request <a name="GetCapabilities request"></a>   | /WMS_Capabilities/Capability/Request/GetCapabilities/DCPType/HTTP/Get/OnlineResource/@xlink:href
