# Conformance class: INSPIRE Profile of ISO 19128 (DRAFT)

This conformance class is part of the [Abstract Test Suite for the INSPIRE View Services Technical Guidance](http://inspire.ec.europa.eu/id/ats/view-service/3.11).

## Standardization target type

OGC web service WMS 1.3.0

## Dependencies

### Direct dependencies

A direct dependency is another conformance class whose requirements must be met by the view service, too.

| Specification | Conformance class | Parameters | 
| ------------- | ----------------- | ---------- |
| [ISO 19128 / OGC WMS 1.3.0](#ref_WMS) | Basic WMS | n/a |

### Indirect dependencies

An indirect dependency is another conformance class whose requirements must be met by a related resource.

| Specification | Conformance class | Related resource | Parameters |
| ------------- | ----------------- | ---------------- | ---------- |
| [Technical Guidance for the implementation of INSPIRE View Services 3.11](#ref_TG_VS) | [Layer metadata](http://inspire.ec.europa.eu/id/ats/view-service/3.11/layer-metadata) | Capabilities document |  `service type` = `ISO 19128` |
 
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

## TG Requirement coverage

Based on requirement numbering in [TG VS](#ref_TG_VS).

| Req#   | Description                          | Covered by test(s)                 | IR reference(s)                  |
| ------ | ------------------------------------ | ---------------------------------- | -------------------------------- |
| 1      | Scoping: ISO 19128 + INSPIRE ext.    | n/a                                | n/a                              |
| 2      | WMS basic conformance class          | OGC WMS 1.3.0. A.1.2 Basic WMS Server, [Schema validation](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/schema-validation)  | n/a  |
| 3      | GetCapabilities, GetMap              | OGC WMS 1.3.0. "WMS basic" CC ATS  | n/a |
| 4      | INSPIRE ExtendedCapabilities         | [Response parameters through service Capabilities](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/response-parameters-through-service-capabilities) | n/a |
| 5      | GetCapabilities request parameters   | OGC WMS 1.3.0. "WMS basic" CC ATS,  | [IR NS](#ref_IR_NS), Annex III, Chapter 2.1.1 |
| 6      | MetadataURL references INSPIRE service metadata | [MetadataURL reference INSPIRE service metadata](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/metadataurl-reference-inspire-service-metadata) |n/a |
| 7      | Use WMS + INSPIRE extended capabilities  | Test bound to specific requirements | n/a |
| 8      | Language section in Extended capabilities |[Supported and response languages node](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/supported-and-response-languages-node) | [IR NS](#ref_IR_NS), Annex III, Chapter 2.2.3 |
| 9      | View Service Metadata in Discovery Service | [View service metadata published in an INSPIRE discovery service](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/in-discovery-service) |  [IR NS](#ref_IR_NS), Annex III, Chapter 4. |
| 10     | Mapping of service metadata elements | [Title and Abstract](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/title-and-abstract), [resource type is service](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/resource-type-is-service), [resource locator](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/resource-locator), [map coupled resource metadata](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/map-coupled-resource-metadata), [map sds type with extendedcapabilitie](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/map-sds-type-with-extendedcapabilities), [keyword node](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/keyword-node), [ex_geographicboundingbox node](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/geographic-bounding-box), [date type](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/date-type), [temporal reference](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/temporal-reference), [degree of conformity](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/degree-of-conformity), [conformity node](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/conformity-node), [fees node](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/fees-node), [contact person](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/contact-person), [contact position](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/contact-position), [point of contact details](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/point-of-contact-details), [metadata date](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/metadata-date) | [IR MD](#ref_IR_MD), Part B |
| 11     | ResourceType element | [Resource type is Service](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/resource-type-is-service) | |
| 12     | ResourceLocator element | [Resource Locator](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/resource-locator) | |
| 15     | SpatialDataServiceType element | [Map SDS Type with ExtendedCapabilities](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/map-sds-type-with-extendedcapabilities) | |
| 16     | Classification of Spatial Data Services keyword | | |
| 17     | Additional keywords | Not testable | |
| 18     | MD keywords | [Keyword node](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/keyword-node) | |
| 19     | Geographic Bounding Box | [EX_geographicboundingbox node](ex_geographicboundingbox node.md) | |
| 20     | Temporal reference dates | [Date type](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/date-type) | |
| 21     | TemporalReference element | [Temporal reference](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/temporal-reference) | |
| 22     | Degree of conformity | [Degree of conformity](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/degree-of-conformity) | |
| 23     | Conformity | [Conformity node](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/conformity-node) | |
| 24     | Conditions of access and use  | [Fees node](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/fees-node) | |
| 25     | Responsible party |  [Contact persone](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/contact-person) | |
| 26     | Responsible party role | [Contact position](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/contact-position) | |
| 27     | Point of contact with name and email | [Point of contact details](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/point-of-contact-details) | |
| 28     | Point of contact in ext. capabilities | [Point of contact details](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/point-of-contact-details) | |
| 29     | Metadata date | [Metadata date](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/metadata-date) | |
| 30     | GetCapabilities operation | [Schema validation](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/schema-validation) | |
| 30     | GetMap Operation | [Getmap format](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/getmap-format) | |
| 32     | Layer metadata | [Title and Abstract](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/title-and-abstract), [keywordlist](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/keywordlist), [Bounding box in layer](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/bbox-in-layer), [layer identifier node](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/layer-identifier-node), [harmonised layer name](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/harmonised-layer-name), [etrs89 or itrs crs](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/etrs89-or-itrs-crs), [inspire default styles](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/inspire-default-styles) | |
| 35     | Additional layer keywords | [Keywordlist](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/keywordlist) | |
| 37     | Unique Resource Identifier (layer origin) | [layer identifier node](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/layer-identifier-node) | |
| 38     | AuthorityURL & Identifier | [Layer identifier node](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/layer-identifier-node) | |
| 40     | Coordinate Reference Systems | [etrs89 or itrs crs](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/etrs89-or-itrs-crs) | |
| 42     | inspire_common:default style | [Inspire default styles](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/inspire-default-styles) | |
| 43     | GCM fallback style | [Review default styles](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/review-default-style) | |
| 44     | inspire_common:default is the default layer Style | [Review default styles](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/review-default-style) | |
| 48     | Layer Dimension elements | Not testable | |
| 49     | Category layers | [Category Layers.md](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/category-layers) | |
| 50     | GetMap: VERSION parameter | OGC WMS 1.3.0. ATS: A.1.2.4 GetMap response | |
| 51     | GetMap: REQUEST parameter | OGC WMS 1.3.0. ATS: A.1.2.4 GetMap response | |
| 52     | GetMap: LAYERS parameter | OGC WMS 1.3.0. ATS: A.1.2.4 GetMap response | |
| 53     | GetMap: STYLES parameter | OGC WMS 1.3.0. ATS: A.1.2.4 GetMap response | |
| 54     | GetMap: CRS parameter | OGC WMS 1.3.0. ATS: A.1.2.4 GetMap response | |
| 55     | GetMap: BBOX parameter | OGC WMS 1.3.0. ATS: A.1.2.4 GetMap response | |
| 56     | GetMap: WIDTH & HEIGHT parameters | OGC WMS 1.3.0. ATS: A.1.2.4 GetMap response | |
| 57     | GetMap: FORMAT parameter | OGC WMS 1.3.0. ATS: A.1.2.4 GetMap response | |
| 58     | GetMap: TRANSPARENT parameter | OGC WMS ATS: 1.3.0. A.1.2.4 GetMap response | |
| 59     | GetMap: EXCEPTIONS parameter | OGC WMS 1.3.0. ATS: A.1.2.4 GetMap response | |
| 60     | Link View Service: scoping | [View service metadata published in an INSPIRE discovery service](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/in-discovery-service) | |
| 61     | Service metadata in Discovery Service |  [View service metadata published in an INSPIRE discovery service](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/in-discovery-service) | |
| 62     | Cascading layers in collated capabilities | [Review cascading view services](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/cascading-view-services) | |
| 63     | Cascaded layers to include "cascaded" attribute | [Review cascading view services](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/cascading-view-services) | |
| 64     | The value of the "cascaded" attribute indicates cascading level | [Review cascading view services](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/cascading-view-services) | |
| 65     | Transparency & background for collated layers | [Review cascading view services](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/cascading-view-services) | |
| 67     | Client may select the language | [Language selection capabilities](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/language-selection-capabilities) | |
| 68     | GetCapabilities: LANGUAGE parameter | [Language selection capabilities](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/language-selection-capabilities) | |
| 69     | GetCapabilities: default language | [Default language](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/default-language) | |
| 70     | ResponseLanguage element | [Language selection capabilities](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/language-selection-capabilities) | [IR NS](#ref_IR_NS), Annex III, Chapter 2.2.3 |
| 71     | SupportedLanguages and DefaultLanguage elements | [Supported and response languages node](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/supported-and-response-languages-node) | [IR NS](#ref_IR_NS), Annex III, Chapter 2.2.3 |
| 72     | ExtendedCapabilities XML Schema | [Response parameters through service Capabilities](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/response-parameters-through-service-capabilities) | |
| 73     | GetMap: Portrayal requiring localized rendering | [Language support for rendered text](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/linguistic-labels) | |

Note: Requirements marked as "not testable" should be reconsidered in a revision of the technical guidance" 

## Two scenarios for providing the service metadata

The [TG VS](#ref_TG_VS) gives two options (scenarios) for providing the service metadata in the Capabilities document of the WMS services:

1. INSPIRE network service metadata in a Discovery Service is referenced through an extended capability.
2. Use (extended) capabilities to map all INSPIRE metadata elements to the WMS 1.3.0 elements.

The requirements considering including the mandatory INSPIRE metadata elements on the Capabilities document depend on which scenario the data provider has chosen to follow. Since there is no dedicated method in [TG VS](#ref_TG_VS) for the data prodiver to indicate which scenario he/she has chosen, the validator software must use the following logic to decide the appropriate set of tests to apply:

The scenario 2 is selected only if at least one of the following elements exists in the WMS Capabilities document's `inspire_vs:ExtendedCapabilities` element:

* `inspire_common:ResourceLocator`,
* `inspire_common:ResourceType`,
* `inspire_common:TemporalReference`,
* `inspire_common:Conformity`,
* `inspire_common:MetadataPointOfContact`,
* `inspire_common:MetadataDate`,
* `inspire_common:SpatialDataServiceType`,
* `inspire_common:MandatoryKeyword`,
* `inspire_common:Keyword`

If none of them is found, the scenario 1 must be selected for the validation.

The the case of scenario 1, the metadata record referred to by the `inspire_common:MetadataUrl` element must also pass the service scenario of the test suite [ATS Metadata](http://inspire.ec.europa.eu/id/ats/metadata/3.1).

## Tests

This Conformance Class contains the following tests. The "scenario" column of the test table below indicates if the tests are to be applied in service metadata validation scenarios 1, 2 or all (see above).

The tests with a prefix "WMS" refer to the ATS included in the [OGC WMS 1.3.0 specification](#ref_WMS) (Annex A).

| Identifier                                                                          | Scenario(s) | Status   |
| ----------------------------------------------------------------------------------- | -------- | -------- |
| WMS.A.1.2.1 Version negotiation | all | final |
| WMS.A.1.2.2 Request parameter rules | all | final |
| WMS.A.1.2.3 GetCapabilities response | all | final |
| WMS.A.1.2.4 GetMap response | all | final |
| [Bounding box in layer](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/bbox-in-layer) | all | ready for review |
| [Category layers](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/category-layers) | all | ready for review |
| [Conformity node](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/conformity-node) | 2 only | ready for review |
| [Contact person](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/contact-person) | all | ready for review |
| [Contact position](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/contact-position) | all | ready for review |
| [Date type](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/date-type) | 2 only | ready for review |
| [Default language](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/default-language) | all | ready for review |
| [Degree of conformity](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/degree-of-conformity) | 2 only | ready for review |
| [ETRS89 or ITRS CRS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/etrs89-or-itrs-crs) | all | ready for review |
| [Fees node](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/fees-node) | all | ready for review |
| [Geographic bounding box](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/geographic-bounding-box) | all | ready for review |
| [GetMap format](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/getmap-format) | all | ready for review |
| [INSPIRE default styles](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/inspire-default-styles) | all | ready for review |
| [Keyword node](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/keyword-node) | 2 only | ready for review |
| [Keyword list](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/keywordlist) | all | ready for review |
| [Language selection capabilities](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/language-selection-capabilities) | all | ready for review |
| [Layer identifier node](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/layer-identifier-node) | all | ready for review |
| [Language support for rendered text](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/linguistic-labels) | all | ready for review |
| [Map coupled resource metadata](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/map-coupled-resource-metadata) | all | ready for review |
| [Map SDS type with ExtendedCapabilities](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/map-sds-type-with-extendedcapabilities) | 2 only | ready for review |
| [Metadata date](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/metadata-date) | 2 only | ready for review |
| [MetadataURL reference INSPIRE service metadata](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/metadataurl-reference-inspire-service-metadata) | 1 only | ready for review |
| [Point-of-contact details](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/point-of-contact-details) | 2 only | ready for review |
| [Resource locator](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/resource-locator) | 2 only | ready for review |
| [Resource type is service](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/resource-type-is-service) | 2 only | ready for review |
| [Review cascading view services](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/cascading-view-services) | all | ready for review |
| [Review default styles](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/review-default-style) | all | ready for review |
| [Schema validation](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/schema-validation) | all | ready for review |
| [Supported and response languages node](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/supported-and-response-languages-node) | all | ready for review |
| [Temporal reference](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/temporal-reference) | 2 only | ready for review |
| [Title and abstract](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/title-and-abstract) | all | ready for review |
| [View service metadata published in an INSPIRE discovery service](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/in-discovery-service) | all | ready for review |

## Open issues

* The requirement 6 for providing a link to the INSPIRE MetadataURL is limited to service metadata scenario 1. However, the requirement 9 states that the View Service metadata must be included in an INSPIRE Discovery regardless of the chosen scenario. Also the Requirements 60 & 61 state that the Link View Service operation is realized by using a Discovery Service. Thus it would make sense that the MetadataURL element if the Service in the ExtendedCapabilities would be mandatory in both scenarios.
* Should the mandatory keyword from the "Classification of Spatial data Services" be also given as wms:Keyword in the Capabilities document under wms:WMS_Capabilities/wms:Service/wms:KeywordList in addition to the ExtendedCapabilities (scenario 2) or in the referenced service metadata record (scenario 1)?

## XML namespace prefixes <a name="namespaces"></a>

The following prefixes are used to refer to the corresponding XML namespaces in all test descriptions:

Prefix         | Namespace
-------------- | -------------------------------------------------
wms            | http://www.opengis.net/wms
xlink          | http://www.w3.org/1999/xlink
gmd            | http://www.isotc211.org/2005/gmd
inspire_vs     | http://inspire.ec.europa.eu/schemas/inspire_vs/1.0
inspire_common | http://inspire.ec.europa.eu/schemas/common/1.0
