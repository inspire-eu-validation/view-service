# Check PNG-GIF image format

**Purpose**: Either PNG or GIF format (without LZW compression) with transparency shall be supported by the View service INS NS, Annex III, Part B. Furthermore, when a layer is requested in one of the supported formats, the response should be encoded in this format.

**Prerequisites**

* [Schema validation](Schema validation.md)

**Test method**

 
* For ISO 19128, check that there is a [Format](#Format) element that contains "image/png" or "image/gif". Make a GetMap request for each [layer](#layer) provided by the service using a maximum allowed bounding box and either "image/png" or "image/gif" format and check that the returned image is encoded in the requested format. If both formats are listed by the GetMap operation metadata, two seperate requests are made. The test case passes when all requests return animage encoded in the requested format.

* For WMTS 1.0.0, check for each [layer](#layer) that there is at least one [Format](#format) element either with content "image/png" or "image/gif". Make a GetTile request for the layer for one tile using either "image/png" or "image/gif" format and check that the returned image is encoded in the requested format. If both formats are listed in the layer metadata, two seperate requests are made. The test case passes when all requests return an image encoded in the requested format.

**Reference(s)**:

* [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.3.2.2, Requirement 31
* [TG VS](README.md#ref_TG_VS), Chapter 5.2.3.3.2.2, Requirement 82

**Test type:** Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                     |  XPath expression												|  Parameter  value
------------------------------------------------ | ---------------------------------------------------------------	| ---------------------------------------------------------------
layer <a name="layer"></a> | /wms:WMS_Capabilities/wms:Capability/wms:Layer | ISO 19128
                           | /wmts:Capabilities/wmts:Contents/wmts:Layer | WMTS 1.0.0
GetMap <a name="GetMap"></a> | /wms:WMS_Capabilities/wms:Capability/wms:Request/wms:GetMap | ISO 19128
Format <a name="format"></a> | /wms:WMS_Capabilities/wms:Capability/wms:Request/wms:GetMap/wms:Format | ISO 19128
                             | /wmts:Capabilities/wmts:Contents/wmts:Layer/wmts:Format | WMTS 1.0.0
