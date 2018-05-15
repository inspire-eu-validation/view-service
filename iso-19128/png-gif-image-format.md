# PNG-GIF image format

**Purpose**: Either PNG or GIF format (without LZW compression) with transparency shall be supported by the View service INS NS, Annex III, Part B. Furthermore, when a layer is requested in one of the supported formats, the response should be encoded in this format.

**Prerequisites**

* [Schema validation](http://inspire.ec.europa.eu/id/ats/view-service/3.11/ISO-19128/schema-validation)

**Test method**

 
* For ISO 19128, check that there is a [Format](#Format) element that contains "image/png" or "image/gif".
* Make a GetMap request for each [layer](#layer) provided by the service using a maximum allowed bounding box and either "image/png" or "image/gif" format and check that the returned image is encoded in the requested format. If both formats are listed by the GetMap operation metadata, two seperate requests are made. The test case passes when all requests return animage encoded in the requested format.

**Reference(s)**:

* [TG VS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/ISO-19128/README#ref_TG_VS), Chapter 4.2.3.3.2.2, Requirement 31


**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/view-service/3.11/ISO-19128/README#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
GetMap <a name="GetMap"></a> | ./wms:Capability/wms:Request/wms:GetMap
Format <a name="format"></a> | ./wms:Capability/wms:Request/wms:GetMap/wms:Format
