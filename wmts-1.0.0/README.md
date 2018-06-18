# Conformance class: INSPIRE Profile of WMTS 1.0.0 (DRAFT)

This conformance class is part of the [Abstract Test Suite for the INSPIRE View Services Technical Guidance](http://inspire.ec.europa.eu/id/ats/view-service/3.11).

## Standardization target type

OGC web service (WMTS 1.0.0)

## Dependencies

### Direct dependencies

A direct dependency is another conformance class whose requirements must be met by the view service, too.

| Specification | Conformance class | Parameters | 
| ------------- | ----------------- | ---------- |
| [WMTS 1.0.0](#ref_WMTS) | Server | n/a |

### Indirect dependencies

An indirect dependency is another conformance class whose requirements must be met by a related resource.

| Specification | Conformance class | Related resource | Parameters |
| ------------- | ----------------- | ---------------- | ---------- |
| [Technical Guidance for the implementation of INSPIRE View Services 3.11](#ref_TG_VS) | [Layer metadata](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata) | Capabilities document |  `service type` = `WMTS 1.0.0` |
 
## External document references

The following abbreviations are used in the test text for referring to external documents:

Abbreviation                     | Document name
-------------------------------- | --------------------------------------------------
INSPIRE <a name="ref_INSPIRE"></a> | [Directive 2007/2/EC of the European Parliament and of the Council of 14 March 2007 establishing an Infrastructure for Spatial Information in the European Community (INSPIRE)](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32007L0002&from=EN)
TG VS <a name="ref_TG_VS"></a>   | [Technical Guidance for the implementation of INSPIRE View Services 3.11](http://inspire.jrc.ec.europa.eu/documents/Network_Services/TechnicalGuidance_ViewServices_v3.11.pdf)
IR NS <a name="ref_IR_NS"></a>   | [Commission Regulation (EC) No 976/2009 of 19 October 2009 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards the Network Services](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32009R0976&from=EN)
IR IOP <a name="ref_IR_IOP"><a/> | [COMMISSION REGULATION (EU) No 1089/2010 of 23 November 2010 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards interoperability of spatial data sets and services](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=OJ:L:2010:323:FULL&from=EN)
WMTS <a name="ref_WMTS"></a>     | [OpenGIS® Web Map Tile Service Implementation Standard version 1.0.0](http://portal.opengeospatial.org/files/?artifact_id=35326)
TG MD <a name="ref_TG_MD"></a>   | [Technical Guidance for the implementation of INSPIRE Discovery Services 3.1](http://inspire.ec.europa.eu/documents/Network_Services/TechnicalGuidance_DiscoveryServices_v3.1.pdf)

## TG Requirement coverage

Based on requirement numbering in [TG VS](#ref_TG_VS).

| Req#  | Description                          | Covered by test(s)                 | IR reference(s)                  |
| ----- | ------------------------------------ | ---------------------------------- | -------------------------------- |
| IR 74 | Scope: WMTS 1.0 + INSPIRE extensions |  n/a                               |                              |
| IR 75 | WMTS GetCapabilities, GetTile       |  All included OGC WMTS tests       |  n/a                             |
| IR 76 | Link View Service                    |  n/a                               |                              |
| IR 77 | Common request parameters            |  WMTS common request parameter tests  | Annex III, Part A, 2.1.1. & 3.1.1. |
| IR 78 | Service metadata content             |  WMTS GetCapabilities tests, most of the tests in this suite   |
| IR 79 | Coupled Resource             |  [Map coupled resource metadata](http://inspire.ec.europa.eu/id/ats/view-service/3.11/WMTS/map-coupled-resource-metadata)   |
| IR 80 | Link View Service                    |  n/a                |                                             |
| IR 81 | GetCapabilities operation metadata   | WMTS.A.3.2.2        |                                            |
| IR 82 | GetTile operation metadata           | [GetTile operation](http://inspire.ec.europa.eu/id/ats/view-service/3.11/WMTS/gettile-languages), [PNG-GIF image format](http://inspire.ec.europa.eu/id/ats/view-service/3.11/WMTS/png-gif-image-format)        |                                             |
| IR 83 | Link View Service operation metadata | n/a                 |                                            |
| IR 84 | Harmonised layer name | [Harmonised Layer Name](http://inspire.ec.europa.eu/id/ats/view-service/3.11/WMTS/harmonised-layer-name) |
| IR 85 | Layer Title | [Layer Title](http://inspire.ec.europa.eu/id/ats/view-service/3.11/WMTS/layer-title) |
| IR 86 | Layer Language | [Layer Language](http://inspire.ec.europa.eu/id/ats/view-service/3.11/WMTS/layer-language) |
| IR 87 | Keywords                             | not testable           | Annex III, Part A, 2.2.4 |
| IR 88 | Minimum Geographic Bbox | [Minimum Geographic Bbox](http://inspire.ec.europa.eu/id/ats/view-service/3.11/WMTS/minimum-geographic-bbox) |
| IR 89 | Use ETRS & ITRS CRSes                | [ETRS89 or ITRS coordinate reference system](http://inspire.ec.europa.eu/id/ats/view-service/3.11/WMTS/etrs89-or-itrs-crs) |  Annex III, Part B, 1.  |
| IR 90 | Layer StyleName           | [Layer Style Name](http://inspire.ec.europa.eu/id/ats/view-service/3.11/WMTS/layer-style-name) | Annex III, Part A, 3.1.1.  |
| IR 92 | GetTile request parameters           | WMTS tests for GetTile, [GetTile language support](http://inspire.ec.europa.eu/id/ats/view-service/3.11/WMTS/gettile-languages) | Annex III, Part A, 3.1.1.  |

Note: Requirements marked as "not testable" should be reconsidered in a revision of the technical guidance" 

## Tests

This Conformance Class contains the tests in the table below. The test with "WMTS" prefix refer to the OGC WMTS 1.0.0 specification ATS (Annex A).

| Identifier                                                                                | Origin | Mechanical | Status   |
| ----------------------------------------------------------------------------------------- | ------ | ---------- | -------- |
| WMTS.A.3.1.2 Accept HTTP GET and POST transferred operation requests (All operations)     | OGC WMTS 1.0.0     | Yes        | Final    |
| WMTS.A.3.1.3 Handle KVP-encoded operation requests (All operations) | OGC WMTS 1.0.0     | Yes        | Final    |
| WMTS.A.3.1.4 Handle SOAP-encoded operation requests (All operations) 	        | OGC WMTS 1.0.0     | Yes        | Final    |
| WMTS.A.3.1.5 Handle HTTP GET RESTful -encoded operation requests (All operations) 	                    | OGC WMTS 1.0.0     | Yes        | Final    |
| WMTS.A.3.1.6 KVP and SOAP HTTP response status code (All operations)                  | OGC WMTS 1.0.0     | Yes        | Final    |
| WMTS.A.3.2.1 Accept HTTP GET transferred operation requests (GetCapabilities) 	                    | OGC WMTS 1.0.0     | Yes        | Final    |
| WMTS.A.3.2.2  GetCapabilities operation response (GetCapabilities)                   | OGC WMTS 1.0.0     | Yes        | Final    |
| WMTS.A.3.2.3 Version negotiation (GetCapabilities)                   | OGC WMTS 1.0.0     | Yes        | Final    |
| WMTS.A.3.2.4 Format selection (GetCapabilities)	                    | OGC WMTS 1.0.0     | Yes        | Final    |
| WMTS.A.3.2.5 Handling updateSequence parameter (GetCapabilities) 	                    | OGC WMTS 1.0.0     | Yes        | Final    |
| WMTS.A.3.2.6 Section selection (GetCapabilities)                   | OGC  WMTS 1.0.0     | Yes        | Final    |
| WMTS.A.3.3.1 Accept HTTP GET transferred operation requests (ServiceMetadata resource)	                    | OGC WMTS 1.0.0     | Yes        | Final    |
| WMTS.A.3.4.1 XML well formated (ServiceMetadata response)      | OGC WMTS 1.0.0     | Yes        | Final    |
| WMTS.A.3.4.2 XML references the normative schema (ServiceMetadata response)     | OGC WMTS 1.0.0     | Yes        | Final    |
| WMTS.A.3.4.3 XML validates against the schema (ServiceMetadata response)     | OGC WMTS 1.0.0      | Yes        | Final    |
| WMTS.A.3.4.4 OnLineResource is an only resource prefix (ServiceMetadata response)     | OGC WMTS 1.0.0      | Yes        | Final    |
| WMTS.A.3.4.5 XML format for GetCapabilities (ServiceMetadata response)      | OGC WMTS 1.0.0      | Yes        | Final    |
| WMTS.A.3.4.6 ows:Constraint GetEncoding (ServiceMetadata response)]     | OGC WMTS 1.0.0      | Yes        | Final    |
| WMTS.A.3.4.7 ows:Constraint PostEncoding (ServiceMetadata response)     | OGC WMTS 1.0.0      | Yes        | Final    |
| WMTS.A.3.4.8 Layer identifiers (ServiceMetadata response)    | OGC WMTS 1.0.0      | Yes        | Final    |
| WMTS.A.3.4.9 Layer LegendURL are correct resources (ServiceMetadata response)     | OGC WMTS 1.0.0      | Yes        | Final    |
| WMTS.A.3.4.10 Layer LegendURL correct Format (ServiceMetadata response)      | OGC WMTS 1.0.0      | Yes        | Final    |
| WMTS.A.3.4.11 Layer LegendURL correct sizes (ServiceMetadata response)      | OGC WMTS 1.0.0      | Yes        | Final    |
| WMTS.A.3.4.12 Layer TileMatrixSet is valid (ServiceMetadata response)     | OGC WMTS 1.0.0      | Yes        | Final    |
| WMTS.A.3.4.13 TileMatrixSet Identifier (ServiceMetadata response)     | OGC WMTS 1.0.0      | Yes        | Final    |
| WMTS.A.3.4.14 TileMatrix Identifier (ServiceMetadata response)    | OGC WMTS 1.0.0      | Yes        | Final    |
| WMTS.A.3.4.15 TileMatrixSet ScaleDenominators (ServiceMetadata response)      | OGC WMTS 1.0.0      | Yes        | Final    |
| WMTS.A.3.4.16 TileMatrixSet WellKnownScaleSet (ServiceMetadata response)      | OGC WMTS 1.0.0      | Yes        | Final    |
| WMTS.A.3.4.17 Theme LayerRef is valid (ServiceMetadata response)      | OGC WMTS 1.0.0      | Yes        | Final    |
| WMTS.A.3.5.1 Layer (GetTile)      | OGC WMTS 1.0.0      | Yes        | Final    |
| WMTS.A.3.5.2 ResourceURL template (GetTile)     | OGC WMTS 1.0.0      | Yes        | Final    |
| WMTS.A.3.5.3 TileMatrixSet (GetTile)    | OGC WMTS 1.0.0      | Yes        | Final    |
| WMTS.A.3.5.4 TileMatrix (GetTile)     | OGC WMTS 1.0.0      | Yes        | Final    |
| WMTS.A.3.5.5 TileRow and TileCol (GetTile)      | OGC WMTS 1.0.0      | Yes        | Final    |
| WMTS.A.3.5.6 Incorrect Style (GetTile)      | OGC WMTS 1.0.0      | Yes        | Final    |
| WMTS.A.3.5.7 Tile incorrect dimension value (GetTile)     | OGC WMTS 1.0.0      | Yes        | Final    |
| WMTS.A.3.5.8 Tile dimension default and current (GetTile)     | OGC WMTS 1.0.0      | Yes        | Final    |
| WMTS.A.3.5.9 Incorrect Format (GetTile)     | OGC WMTS 1.0.0      | Yes        | Final    |
| WMTS.A.3.5.10 Correct Format (GetTile)      | OGC WMTS 1.0.0      | Yes        | Final    |
| WMTS.A.3.5.11 Size (GetTile)      | OGC WMTS 1.0.0      | Yes        | Final    |
| WMTS.A.3.5.12 Transparent color (GetTile)      | OGC WMTS 1.0.0      | Yes        | Final
| [GetTile operation](http://inspire.ec.europa.eu/id/ats/view-service/3.11/wmts-1.0.0/gettile-languages) | IR | Yes | Ready for review
| [etrs89 or itrs crs](http://inspire.ec.europa.eu/id/ats/view-service/3.11/wmts-1.0.0/etrs89-or-itrs-crs) | IR | Yes | Ready for review
| [Map coupled resource metadata](http://inspire.ec.europa.eu/id/ats/view-service/3.11/WMTS/map-coupled-resource-metadata)   | IR | Yes | Ready for review
| [GetTile operation](http://inspire.ec.europa.eu/id/ats/view-service/3.11/WMTS/gettile-languages)| IR | Yes | Ready for review
| [PNG-GIF image format](http://inspire.ec.europa.eu/id/ats/view-service/3.11/WMTS/png-gif-image-format)| IR | Yes | Ready for review
| [Harmonised Layer Name](http://inspire.ec.europa.eu/id/ats/view-service/3.11/WMTS/harmonised-layer-name)| IR | Yes | Ready for review
| [Layer Title](http://inspire.ec.europa.eu/id/ats/view-service/3.11/WMTS/layer-title)| IR | Yes | Ready for review
| [Layer Language](http://inspire.ec.europa.eu/id/ats/view-service/3.11/WMTS/layer-language)| IR | Yes | Ready for review
| [Minimum Geographic Bbox](http://inspire.ec.europa.eu/id/ats/view-service/3.11/WMTS/minimum-geographic-bbox)| IR | Yes | Ready for review
| [ETRS89 or ITRS coordinate reference system](http://inspire.ec.europa.eu/id/ats/view-service/3.11/WMTS/etrs89-or-itrs-crs)| IR | Yes | Ready for review
| [Layer Style Name](http://inspire.ec.europa.eu/id/ats/view-service/3.11/WMTS/layer-style-name)| IR | Yes | Ready for review
| [GetTile language support](http://inspire.ec.europa.eu/id/ats/view-service/3.11/WMTS/gettile-languages)| IR | Yes | Ready for review

## Open issues

* There are no explicit requirements for including any of the INSPIRE ServiceMetadata elements in the Capabilities document, thus there is are no test for the existence of these elements either. This is probably not intended by the TG authors.

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix           | Namespace
---------------- | -------------------------------------------------
wmts             | http://www.opengis.net/wmts/1.0
ows              | http://www.opengis.net/ows/1.1
inspire_vs       | http://inspire.ec.europa.eu/schemas/inspire_vs/1.0
inspire_common   | http://inspire.ec.europa.eu/schemas/common/1.0
gmd              | http://www.isotc211.org/2005/gmd
gco              | http://www.isotc211.org/2005/gco
csw              | http://www.opengis.net/cat/csw/2.0.2
xlink            | http://www.w3.org/1999/xlink
