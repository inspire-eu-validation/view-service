# Map Coupled Resource metadata

**Purpose**: Coupled Resource shall be mapped to the `MetadataURL` elements of the Layer elements of the service capabilities. 
If linkage to the data sets or series on which the service operates are available, then the linkage to these resources shall 
be provided as stated by the INSPIRE Metadata Technical Guidance INS MDTG.

**Prerequisites**

* [Schema validation](http://inspire.ec.europa.eu/id/ats/view-service/3.11/WMTS/schema-validation)

**Test method**

* If there is a MetadataURL node for a layer:
  * Verify that the response to a HTTP GET request of the URL in [OnlineResource/@xlink:href](#OnlineResource) of the MetadataURL section is an XML document with a root element csw:GetRecordByIdResponse or gmd:MD_Metadata.
  * In case of a csw:GetRecordByIdResponse document, use the first [gmd:MD_Metadata](#Metadata) child element. Issue an error if there is no such element.

**Reference(s)**:
* [TG VS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/WMTS/README#ref_TG_VS), Chapter 5.2.3.1, Requirement 79

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/view-service/3.11/WMTS/README#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
MetadataURL <a name="MetadataURL"></a>   | ./wms:Capability/wms:Layer/MetadataURL
OnlineResource/@xlink:href <a name="OnlineResource"></a>   | ./wms:Capability/wms:Layer/MetadataURL/Format/OnlineResource[@xlink:href='http://www.w3.org/1999/xlink']
Metadata <a name="Metadata"></a>  | gmd:MD_Metadata/gmd:distributionInfo/\*/gmd:transferOptions/gmd:MD_DigitalTransferOptions/ \*/gmd:CI_OnlineResource[1]