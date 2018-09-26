# Schema validation

**Purpose**: The operation for implementing INSPIRE Get View Service Metadata operation is the GetCapabilities operation. The parameters defined within the ISO 19128 standard shall be used to convey relevant information in order to get the expected responses as described in INS NS, Annex III, Section 2.2 of the Regulation on INSPIRE Network Services.

**Prerequisites**

**Test method**

* First check if the [INSPIRE View Service 1.0 schema](http://inspire.ec.europa.eu/schemas/inspire_vs/1.0/inspire_vs.xsd) is given in the service capabilities
* Then check that the GetCapabilities request result validates against this schema.

**Reference(s)**: 

[TG VS](./README#ref_TG_VS), Chapter 4.2.3.2

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
service capabilities <a name="service Capabilities"></a>   | ./@xsi:schemaLocation
GetCapabilities request <a name="GetCapabilities request"></a>   | ./wms:Capability/wms:Request/wms:GetCapabilities/wms:DCPType/wms:HTTP/wms:Get/wms:OnlineResource[@xlink:href]
