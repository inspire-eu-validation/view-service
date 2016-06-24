# Map Coupled Resource metadata

**Purpose**: Coupled Resource shall be mapped to the metadata elements of the Layer elements of the service capabilities (ISO 19128: wms:MetadataURL, WMTS 1.0.0: ows:Metadata). If linkage to the data sets or series on which the service operates are available, then the linkage to these resources shall be provided as stated by the INSPIRE Metadata Technical Guidance INS MDTG.

**Prerequisites**

* [Schema validation](Schema validation.md)

**Test method**

For each [layer](#layer) provided by the service according to it's Service Metadata:

* For ISO 19128: If there is a [MetadataURL](#MetadataURL) for a layer, check that it meets the following conditions. For WMTS 1.0.0: Check that there is at least one [MetadataURL](#MetadataURL) for each layer that meets the following conditions.
  * The URL in [href](#href) resolves.
  * Verify that the response is an XML document with a root element csw:GetRecordByIdResponse or gmd:MD_Metadata.
  * In case of a csw:GetRecordByIdResponse document, check that there is exactly one gmd:MD_Metadata element in the document. Issue an error if there is no such element.

**Reference(s)**:

* [TG VS](README.md#ref_TG_VS) 4.2.3.3.1.5, Requirements 13, 14
* [TG VS](README.md#ref_TG_VS) 5.2.3.1, Requirement 79

**Test type**:

Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                     |  XPath expression												|  Parameter  value
------------------------------------------------ | ---------------------------------------------------------------	| ---------------------------------------------------------------
layer <a name="layer"></a> | /wms:WMS_Capabilities/wms:Capability/wms:Layer | ISO 19128
                           | /wmts:Capabilities/wmts:Contents/wmts:Layer | WMTS 1.0.0
MetadataURL <a name="MetadataURL"></a>   | /wms:WMS_Capabilities/wms:Capability/wms:Layer/wms:MetadataURL | ISO 19128
                                         | /wmts:Capabilities/wmts:Contents/wmts:Layer/ows:Metadata | WMTS 1.0.0
href <a name="href"></a>   | /wms:WMS_Capabilities/wms:Capability/wms:Layer/wms:MetadataURL/wms:Format/wms:OnlineResource/@xlink:href | ISO 19128
                           | /wmts:Capabilities/wmts:Contents/wmts:Layer/ows:Metadata/@xlink:href | WMTS 1.0.0
