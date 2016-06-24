# Harmonised layer name

**Purpose**: It must be unambiguous to find out which of the layers provided by the service visualize the INSPIRE spatial data sets given in the Data Specifications for each INSPIRE theme. These layers must be named according to the INSPIRE Harmonised layer names defined in [TG VS](README.md#ref_TG_VS).

**Prerequisites**

* [Schema validation](Schema validation.md)
* [Map Coupled Resource metadata](Map Coupled Resource metadata.md)

**Test method**

For each [layer](#layer) provided by the service according to it's Service Metadata:

* If there are one or more [MetadataURL](#MetadataURL) for the layer, check that at least one meets the following conditions.
  * The URL in [href](#href) resolves.
  * Verify that the response is an XML document with a root element csw:GetRecordByIdResponse or gmd:MD_Metadata.
  * In case of a csw:GetRecordByIdResponse document, check that there is exactly one gmd:MD_Metadata element in the document. Issue an error if there is no such element.
  * Check if the [Specification](#specification) contains one of the official translations of the names of [TG VS](README.md#ref_TG_VS) and that the value of [Pass](#pass) equals "true".
  * Check that the trimmed string content of the [Name element](#name) matches one the harmonised layer names given in [TG VS](README.md#ref_TG_VS) or it's amendments.
* If in the end each of the layers is either skipped or passed, the test passes.
* If there are more than one layer with the [Metadata element](#metadata) pointing to the same INSPIRE metadata record, the [Identifier](#identifier) of only one of them needs to match one of the harmonised layer names in order for the test to pass for all of those layers.

**Reference(s)**

* [TG VS](README.md#ref_TG_VS), chapters 4.2.3.3.4.6, Requirement 39
* [TG VS](README.md#ref_TG_VS), chapters 5.2.3.3.4.5 and 5.2.3.3.4.6, Requirement 84


**Test type**: Automated

**Notes**

Note 1: The harmonised names only apply to the harmonised INSPIRE datasets provided according to the INSPIRE Data Specifications.

Note 2: The use and usefulness of the harmonised layer names and titles is under discussion, see https://ies-svn.jrc.ec.europa.eu/issues/2172 and https://ies-svn.jrc.ec.europa.eu/projects/miwp-20

Note 3: It's assumed that there may be layers providing portrayals for both the INSPIRE datasets and non-INSPIRE data sets in the same service. Also it's assumed, that there may be more than one layer portraying the same dataset and thus pointing to the same metadata record using the [MetadataURL element](#metadata).

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
Specification <a name="specification"></a> |  /gmd:MD_Metadata/gmd:dataQualityInfo/gmd:DQ_DataQuality/gmd:report/gmd:DQ_DomainConsistency/gmd:result/gmd:DQ_ConformanceResult/gmd:specification/gmd:CI_Citation/gmd:title/gco:CharacterString | *
Pass <a name="pass"></a> |  /gmd:MD_Metadata/gmd:dataQualityInfo/gmd:DQ_DataQuality/gmd:report/gmd:DQ_DomainConsistency/gmd:result/gmd:DQ_ConformanceResult/gmd:pass/gco:Boolean | *
Name element <a name="name"></a> | /wms:WMS_Capabilities/wms:Capability/wms:Layer/wms:Name | ISO 19128
                                 | /wmts:Capabilities/wmts:Contents/wmts:Layer/ows:Identifier | WMTS 1.0.0
