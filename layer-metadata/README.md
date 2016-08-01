# Conformance class: INSPIRE Layer Metadata (DRAFT)

This conformance class is part of the [Abstract Test Suite for the INSPIRE View Services Technical Guidance](http://inspire.ec.europa.eu/id/ats/view-service/3.11).

## Standardization target type

All requirements of a conformance class apply to a single resource type, the standardization target type:

* OGC Capabilities document

## Parameters

A Conformance class may be parameterized, i.e. the class’s tests depend on some parameter that must be defined before the tests can be executed.
 
| Parameter | Values | Description |
| --------- | ------ | ----------- |
| `service type` | `ISO 19128` `WMTS 1.0.0` | The profile implemented by the view service | 

## Dependencies

### Direct dependencies

none

### Indirect dependencies

none
 
## External document references

| Abbreviation | Document name                       |
| ------------ | ----------------------------------- |
| INSPIRE <a name="ref_INSPIRE"></a> | [Directive 2007/2/EC of the European Parliament and of the Council of 14 March 2007 establishing an Infrastructure for Spatial Information in the European Community (INSPIRE)](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32007L0002&from=EN)
| TG VS <a name="ref_TG_VS"></a>   | [Technical Guidance for the implementation of INSPIRE View Services 3.11](http://inspire.jrc.ec.europa.eu/documents/Network_Services/TechnicalGuidance_ViewServices_v3.11.pdf)
| IR NS <a name="ref_IR_NS"></a>   | [Commission Regulation (EC) No 976/2009 of 19 October 2009 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards the Network Services](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32009R0976&from=EN)
| IR MD <a name="ref_IR_MD"></a>   | [COMMISSION REGULATION (EC) No 1205/2008 of 3 December 2008 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards metadata](http://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2008:326:0012:0030:EN:PDF)
| TG MD <a name="ref_TG_MD"></a> | [INSPIRE Metadata Implementing Rules: Technical Guidelines based on EN ISO 19115 and EN ISO 19119](http://inspire.ec.europa.eu/documents/Metadata/MD_IR_and_ISO_20131029.pdf)
| IR IOP <a name="ref_IR_IOP"><a/> | [COMMISSION REGULATION (EU) No 1089/2010 of 23 November 2010 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards interoperability of spatial data sets and services](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=OJ:L:2010:323:FULL&from=EN)
| WMS <a name="ref_WMS"></a>     | [OpenGIS Web Map Service (WMS) Implementation Specification, version 1.3.0](http://portal.opengeospatial.org/files/?artifact_id=14416)
| WMTS <a name="ref_WMTS"></a>     | [OpenGIS® Web Map Tile Service Implementation Standard version 1.0.0](http://portal.opengeospatial.org/files/?artifact_id=35326)


## TG Requirement coverage

Based on requirement numbering in [TG VS](#ref_TG_VS).

### ISO 19128 Profile

| Req#   | Description                          | Covered by test(s)                 | IR reference(s)                  |
| ------ | ------------------------------------ | ---------------------------------- | -------------------------------- |
| 6      | Extended capabilities element exists | [Extended Capabilities](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/extended-capabilities) | |
| 13     | Coupled Resources | [Map Coupled Resource metadata](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/map-coupled-resource-metadata) | |
| 14     | MetadataURL is provided | [Map Coupled Resource metadata](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/map-coupled-resource-metadata) | |
| 31     | Supported image formats for GetMap | [PNG-GIF image format](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/png-gif-image-format) | |
| 33     | Layer contains title (wms) | [layer title](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/layer-title) | |
| 34     | Abstract to describe layer (wms) | [layer language](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/layer-language) | |
| 36     | Geographic Bounding Box for WMS | [Minimum geographic bbox](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/minimum-geographic-bbox) | IR Annex III, Part A, Chapter 2.2.4 |
| 39     | Layer name | [Harmonised layer name](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/harmonised-layer-name) | IR IOP Article 14 |
| 41     | Layer style contains title and identifier | [Layer style name](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/layer-style-name) | IR Annex III, Part A, Chapter 2.2.4 |
| 45     | A legend is provided for layers |[Data visualization legend layer](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/data-visualization-legend-layer)  | |
| 46     | Layer style are mapped correctly (wms) | [layer style name](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/layer-style-name) | IR Annex III, Part A, Chapter 2.2.4 |
| 47     | Internationalized layer legends | [Data visualization legend layer](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/data-visualization-legend-layer)  | |
| 66     | Supported languages | [Supported and response languages node](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/supported-and-response-languages-node) | IR Annex III, Part A, Chapter 2.2.3 |

### WMTS 1.0.0 Profile

| Req#   | Description                          | Covered by test(s)                 | IR reference(s)                  |
| ------ | ------------------------------------ | ---------------------------------- | -------------------------------- |
| 79     | Link to metadata description | [Map Coupled Resource metadata](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/map-coupled-resource-metadata) | |
| 82     | Supported image formats for GetTile | [PNG-GIF image format](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/png-gif-image-format) | |
| 84     | Layer name | [Harmonised layer name](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/harmonised-layer-name) | IR IOP Article 14 |
| 85     | Layer contains title (wmts) | [layer title](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/layer-title) | |
| 86     | Abstract to describe layer (wmts) | [layer language](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/layer-language) | |
| 88     | Geographic Bounding Box for WMTS | [Minimum geographic bbox](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/minimum-geographic-bbox) | IR Annex III, Part A, Chapter 2.2.4 |
| 90     | Layer style are mapped correctly (wmts) | [layer style name](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/layer-style-name) | IR Annex III, Part A, Chapter 2.2.4 |
| 91     | A legend is provided for layers | [Data visualization legend layer](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/data-visualization-legend-layer) | |


## Tests

This Conformance Class contains the following tests.

| Identifier                                                                          | Status   |
| ----------------------------------------------------------------------------------- | -------- |
| [Schema validation](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/schema-validation) | Ready for review |
| [Map Coupled Resource metadata](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/map-coupled-resource-metadata) | Ready for review |
| [Extended Capabilities](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/extended-capabilities) | Ready for review |
| [PNG-GIF image format](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/png-gif-image-format) | Ready for review |
| [Select language capabilities](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/select-language-capabilities) | Ready for review |
| [Supported and response languages node](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/supported-and-response-languages-node) | Ready for review |
| [Layer language](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/layer-language) | Ready for review |
| [Minimum geographic bbox](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/minimum-geographic-bbox) | Ready for review |
| [Harmonised layer name](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/harmonised-layer-name) | Ready for review |
| [Data visualization legend layer](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/data-visualization-legend-layer) | Ready for review |
| [Layer style name](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/layer-style-name) | Ready for review |
| [Layer title](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata/layer-title) | Ready for review |

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
wms            | http://www.opengis.net/wms
xlink          | http://www.w3.org/1999/xlink
gmd            | http://www.isotc211.org/2005/gmd
inspire_vs     | http://inspire.ec.europa.eu/schemas/inspire_vs/1.0
inspire_common | http://inspire.ec.europa.eu/schemas/common/1.0
