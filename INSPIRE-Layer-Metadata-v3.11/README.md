INSPIRE Layer Metadata v3.11
============================

Conformance Class for INSPIRE Layer Metadata v3.11

*Note*: This CC is in Ready for review stage, none of the tests have an official INSPIRE MIG approval.

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

| Req#   | Description                          | Covered by test(s)                 | IR reference(s)                  |
| ------ | ------------------------------------ | ---------------------------------- | -------------------------------- |
| 6      | Extended capabilities element exists | [Check Extended Capabilities](Check Extended Capabilities.md) | |
| 13     | Coupled Resources | [Map Coupled Resource metadata](Map Coupled Resource metadata.md) | |
| 14     | MetadataURL is provided | [Map Coupled Resource metadata](Map Coupled Resource metadata.md) | |
| 31     | Supported image formats for GetMap | [Check PNG-GIF image format](Check PNG-GIF image format.md) | |
| 33     | Layer contains title (WMS) | [Layer title](Layer title.md) | |
| 34     | Abstract to describe layer (WMS) | [Check layer language](Check layer language.md) | |
| 36     | Geographic Bounding Box for WMS | [Minimum geographic bbox](Minimum geographic bbox.md) | IR Annex III, Part A, Chapter 2.2.4 |
| 39     | Layer name | [Harmonised layer name](Harmonised layer name.md) | IR IOP Article 14 |
| 41     | Layer style contains title and identifier | [Layer style name](Layer style name.md) | IR Annex III, Part A, Chapter 2.2.4 |
| 45     | A legend is provided for layers |[Data visualization legend layer](Data visualization legend layer)  | |
| 46     | Layer style are mapped correctly (WMS) | [Layer style name](Layer style name.md) | IR Annex III, Part A, Chapter 2.2.4 |
| 47     | Internationalized layer legends | [Data visualization legend layer](Data visualization legend layer)  | |
| 66     | Supported languages | [Check supported and response languages node](Check supported and response languages node.md) | IR Annex III, Part A, Chapter 2.2.3 |
| 79     | Link to metadata description | [Map Coupled Resource metadata](Map Coupled Resource metadata.md) | |
| 82     | Supported image formats for GetTile | [Check PNG-GIF image format](Check PNG-GIF image format.md) | |
| 84     | Layer name | [Harmonised layer name](Harmonised layer name.md) | IR IOP Article 14 |
| 85     | Layer contains title (WMTS) | [Layer title](Layer title.md) | |
| 86     | Abstract to describe layer (WMTS) | [Check layer language](Check layer language.md) | |
| 88     | Geographic Bounding Box for WMTS | [Minimum geographic bbox](Minimum geographic bbox.md) | IR Annex III, Part A, Chapter 2.2.4 |
| 90     | Layer style are mapped correctly (WMTS) | [Layer style name](Layer style name.md) | IR Annex III, Part A, Chapter 2.2.4 |
| 91     | A legend is provided for layers | [Data visualization legend layer](Data visualization legend layer.md) | |


## Tests

This Conformance Class contains the following tests. The "scenario" column of the test table below indicates if the tests are to be applied in service metadata validation scenarios 1, 2 or all (see above).

The tests with a prefix "WMS" refer to the ATS included in the [OGC WMS 1.3.0 specification](#ref_WMS) (Annex A).

| Identifier                                                                          | Status   |
| ----------------------------------------------------------------------------------- | -------- |
| [Schema validation](Schema validation.md) | Ready for review |
| [Map Coupled Resource metadata](Map Coupled Resource metadata.md) | Ready for review |
| [Check Extended Capabilities](Check Extended Capabilities.md) | Ready for review |
| [Check PNG-GIF image format](Check PNG-GIF image format.md) | Ready for review |
| [Select language capabilities](Select language capabilities.md) | Ready for review |
| [Check supported and response languages node](Check supported and response languages node.md) | Ready for review |
| [Check layer language](Check layer language.md) | Ready for review |
| [Minimum geographic bbox](Minimum geographic bbox.md) | Ready for review |
| [Harmonised layer name](Harmonised layer name.md) | Ready for review |
| [Data visualization legend layer](Data visualization legend layer) | Ready for review |
| [Layer style name](Layer style name.md) | Ready for review |
| [Layer title](Layer title.md) | Ready for review |

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
wms            | http://www.opengis.net/wms
xlink          | http://www.w3.org/1999/xlink
gmd            | http://www.isotc211.org/2005/gmd
inspire_vs     | http://inspire.ec.europa.eu/schemas/inspire_vs/1.0
inspire_common | http://inspire.ec.europa.eu/schemas/common/1.0
