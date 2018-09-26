# Getmap format

**Purpose**: GetMap operation metadata shall be mapped to the wms:GetMap element in the GetCapabilities response. Either PNG or GIF format (without LZW compression) with transparency shall be supported by the View service INS NS, Annex III, Part B. Furthermore, when a layer is requested in one of the supported formats, the response should be encoded in this format.

**Prerequisites**

* [Schema validation](./schema-validation.md)

**Test method**

* Check if there is a [GetMap](#GetMap) node in the Request section of the GetCapabilities response.
* If yes, check whether the GetMap node contains a [Format](#Format) element containing "image/png" and/or "image/gif".
* If this is the case, make a GetMap request for the layer using a maximum allowed bounding box and either "image/png" or "image/gif" format and check that the returned image is [encoded](#encoded) in the requested format. If both formats are listed by the GetMap operation metadata, two seperate requests shall be made. The test case passess when all GetMap requests return a layer encoded in the requested format.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.2.2, Requirement 31 

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
GetMap <a name="GetMap"></a> | ./wms:Capability/wms:Request/wms:GetMap
Format <a name="Format"></a> | ./wms:Capability/wms:Request/wms:GetMap[1]/wms:Format
Format Encoded <a name="Encoded"></a> | ./wms:Capability/wms:Request/wms:GetMap[1]/wms:Format/text()
