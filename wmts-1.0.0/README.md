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

| Req#  | Description                          | Covered by test(s)                 |
| ----- | ------------------------------------ | ---------------------------------- |
| IR 74 | WMTS XML schema validation | [at74-wmts-schema-validation](./at74-wmts-schema-validation.md)
| IR 75 | Implemented Operations | [at75-implemented-operations](./at75-implemented-operations.md)
| IR 76 | Link View Service Operation | [at76-link-view-service-operation](./at76-link-view-service-operation.md)
| IR 77 | Common request parameters | [at77-common-request-parameters](./at77-common-request-parameters.md)
| IR 78 | Get View Service Matadata | [at78-getcapabilities-get-view-service-metadata](./at78-getcapabilities-get-view-service-metadata.md)
| IR 79 | Layer Metadata | [at79-getcapabilities-layer-metadata](./at79-getcapabilities-layer-metadata.md)
| IR 80 | Link View Service | [at80-getcapabilities-link-view-service](./at80-getcapabilities-link-view-service.md)
| IR 81 | Operation GetCapabilities | [at81-getcapabilities-operation-getcapabilities](./at81-getcapabilities-operation-getcapabilities.md)
| IR 82 | Operation GetTile | [at82-getcapabilities-operation-gettile](./at82-getcapabilities-operation-gettile.md)
| IR 83 | Operation Discover Metadata | [at83-getcapabilities-operation-discovermetadata](./at83-getcapabilities-operation-discovermetadata.md)
| IR 84 | Layer Metadata | [at84-getcapabilities-layer-metadata](./at84-getcapabilities-layer-metadata.md)
| IR 85 | Layer Resource Title | [at85-getcapabilities-layer-title](./at85-getcapabilities-layer-title.md)
| IR 86 | Layer Abstract | [at86-getcapabilities-layer-abstract](./at86-getcapabilities-layer-abstract.md)
| IR 87 | Layer Keywords | [at87-getcapabilities-layer-keyword](./at87-getcapabilities-layer-keyword.md)
| IR 88 | Layer Geographic Bounding Box | [at88-getcapabilities-layer-geographic-bounding-box](./at88-getcapabilities-layer-geographic-bounding-box.md)
| IR 89 | ETRS89 or ITRS coordinate reference system | [at89-getcapabilities-etrs89-itrs-crs](./at89-getcapabilities-etrs89-itrs-crs.md)
| IR 90 | Layer Style Title and Identifier | [at90-getcapabilities-layer-style](./at90-getcapabilities-layer-style.md)
| IR 91 | Layer Style Legend URL | [at91-getcapabilities-layer-legend-url](./at91-getcapabilities-layer-legend-url.md)
| IR 92 | GetTile Operation | [at92-gettile-gettile-operation](./at92-gettile-gettile-operation.md)

## Tests

This Conformance Class contains the tests in the table below. 
Besides with these tests, this Conformance Class must be compliant with the tests defined in the OGC WMTS 1.0.0 specification ATS (Annex A).

| Identifier                                                                                | Origin | Type | Status   |
| ----------------------------------------------------------------------------------------- | ------ | ---------- | -------- |
| [at74-wmts-schema-validation](./at74-wmts-schema-validation.md) | IR | Automated | Ready for review
| [at75-implemented-operations](./at75-implemented-operations.md) | IR | Automated | Ready for review
| [at76-link-view-service-operation](./at76-link-view-service-operation.md) | IR | None | Ready for review
| [at77-common-request-parameters](./at77-common-request-parameters.md) | IR | Automated | Ready for review
| [at78-getcapabilities-get-view-service-metadata](./at78-getcapabilities-get-view-service-metadata.md) | IR | Automated | Ready for review
| [at79-getcapabilities-layer-metadata](./at79-getcapabilities-layer-metadata.md) | IR | Automated | Ready for review
| [at80-getcapabilities-link-view-service](./at80-getcapabilities-link-view-service.md) | IR | None | Ready for review
| [at81-getcapabilities-operation-getcapabilities](./at81-getcapabilities-operation-getcapabilities.md) | IR | Automated | Ready for review
| [at82-getcapabilities-operation-gettile](./at82-getcapabilities-operation-gettile.md) | IR | Automated | Ready for review
| [at83-getcapabilities-operation-discovermetadata](./at83-getcapabilities-operation-discovermetadata.md) | IR | None | Ready for review
| [at84-getcapabilities-layer-metadata](./at84-getcapabilities-layer-metadata.md) | IR | Automated | Ready for review
| [at85-getcapabilities-layer-title](./at85-getcapabilities-layer-title.md) | IR | Automated | Ready for review
| [at86-getcapabilities-layer-abstract](./at86-getcapabilities-layer-abstract.md) | IR | Automated | Ready for review
| [at87-getcapabilities-layer-keyword](./at87-getcapabilities-layer-keyword.md) | IR | Automated | Ready for review
| [at88-getcapabilities-layer-geographic-bounding-box](./at88-getcapabilities-layer-geographic-bounding-box.md) | IR | Automated | Ready for review
| [at89-getcapabilities-etrs89-itrs-crs](./at89-getcapabilities-etrs89-itrs-crs.md) | IR | Manual | Ready for review
| [at90-getcapabilities-layer-style](./at90-getcapabilities-layer-style.md) | IR | Automated | Ready for review
| [at91-getcapabilities-layer-legend-url](./at91-getcapabilities-layer-legend-url.md) | IR | Automated | Ready for review
| [at92-gettile-gettile-operation](./at92-gettile-gettile-operation.md) | IR | Automated | Ready for review

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
