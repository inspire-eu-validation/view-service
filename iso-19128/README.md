# Conformance class: INSPIRE Profile of ISO 19128 (DRAFT)

This conformance class is part of the [Abstract Test Suite for the INSPIRE View Services Technical Guidance](../../).

## Standardization target type

OGC web service (WMS 1.3.0)

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
| [Technical Guidance for the implementation of INSPIRE View Services 3.11](#ref_TG_VS) | [Layer metadata](.) | Capabilities document |  `service type` = `ISO 19128` |
 
## External document references

| Abbreviation | Document name                       |
| ------------ | ----------------------------------- |
| INSPIRE <a name="ref_INSPIRE"></a> | [Directive 2007/2/EC of the European Parliament and of the Council of 14 March 2007 establishing an Infrastructure for Spatial Information in the European Community (INSPIRE)](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32007L0002&from=EN)
| TG VS <a name="ref_TG_VS"></a>   | [Technical Guidance for the implementation of INSPIRE View Services 3.11](http://inspire.jrc.ec.europa.eu/documents/Network_Services/TechnicalGuidance_ViewServices_v3.11.pdf)
| IR NS <a name="ref_IR_NS"></a>   | [Commission Regulation (EC) No 976/2009 of 19 October 2009 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards the Network Services](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32009R0976&from=EN)
| IR MD <a name="ref_IR_MD"></a>   | [COMMISSION REGULATION (EC) No 1205/2008 of 3 December 2008 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards metadata](http://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2008:326:0012:0030:EN:PDF)
| TG MD <a name="ref_TG_MD"></a> | [INSPIRE Metadata Implementing Rules: Technical Guidelines based on EN ISO 19115 and EN ISO 19119](http://inspire.ec.europa.eu/documents/Metadata/MD_IR_and_ISO_20131029.pdf)
| IR IOP <a name="ref_IR_IOP"></a> | [COMMISSION REGULATION (EU) No 1089/2010 of 23 November 2010 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards interoperability of spatial data sets and services](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=OJ:L:2010:323:FULL&from=EN)
| WMS <a name="ref_WMS"></a>     | [OpenGIS Web Map Service (WMS) Implementation Specification, version 1.3.0](http://portal.opengeospatial.org/files/?artifact_id=14416)
| INS MD <a name="ref_INS_MD"></a> | [COMMISSION REGULATION (EC) No 1205/2008 of 3 December 2008 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards metadata](https://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32008R1205&qid=1537886135721&from=EN)

## TG Requirement coverage

Based on requirement numbering in [TG VS](#ref_TG_VS).

| Req#   | Description                          | Covered by test(s)                 | IR reference(s)                  |
| ------ | ------------------------------------ | ---------------------------------- | -------------------------------- |
| 1      | Scoping: ISO 19128 + INSPIRE ext.    | n/a                                | n/a                              |
| 2      | WMS basic conformance class          | OGC WMS 1.3.0. A.1.2 Basic WMS Server, [Schema validation](./schema-validation.md)  | n/a  |
| 3      | GetCapabilities, GetMap              | OGC WMS 1.3.0. "WMS basic" CC ATS  | n/a |
| 4      | INSPIRE ExtendedCapabilities         | [Response parameters through service Capabilities](./response-parameters-through-service-capabilities.md) | n/a |
| 5      | GetCapabilities request parameters   | OGC WMS 1.3.0. "WMS basic" CC ATS,  | [IR NS](#ref_IR_NS), Annex III, Chapter 2.1.1 |
| 6      | MetadataURL references INSPIRE service metadata | [MetadataURL reference INSPIRE service metadata](./metadataurl-reference-inspire-service-metadata) |n/a |
| 7      | Use WMS + INSPIRE extended capabilities  | Test bound to specific requirements | n/a |
| 8      | Language section in Extended capabilities |[Supported and response languages node](./supported-and-response-languages-node.md) | [IR NS](#ref_IR_NS), Annex III, Chapter 2.2.3 |
| 9      | View Service Metadata in Discovery Service | [View service metadata published in an INSPIRE discovery service](./in-discovery-service.md) |  [IR NS](#ref_IR_NS), Annex III, Chapter 4. |
| 10     | Mapping of service metadata elements | [Title and Abstract](./title-and-abstract.md), [resource type is service](./resource-type-is-service.md), [resource locator](./resource-locator.md), [map coupled resource metadata](./map-coupled-resource-metadata.md), [map sds type with extendedcapabilities](./map-sds-type-with-extendedcapabilities.md), [keyword node](./keyword-node.md), [ex_geographicboundingbox node](./geographic-bounding-box.md), [date type](./date-type.md), [temporal reference](./temporal-reference.md), [degree of conformity](./degree-of-conformity.md), [fees node](./fees-node.md), [contact person](./contact-person.md), [contact position](./contact-position.md), [point of contact details](./point-of-contact-details.md), [metadata date](./metadata-date.md) | [IR MD](#ref_IR_MD), Part B |
| 11     | ResourceType element | [Resource type is Service](./resource-type-is-service.md) | |
| 12     | ResourceLocator element | [Resource Locator](./resource-locator.md) | |
| 13     | Coupled Resource | [Map coupled resource metadata](./map-coupled-resource-metadata.md) | |
| 14     | Coupled Resource | [Map coupled resource metadata](./map-coupled-resource-metadata.md) | |
| 15     | SpatialDataServiceType element | [Map SDS Type with ExtendedCapabilities](./map-sds-type-with-extendedcapabilities.md) | |
| 16     | Classification of Spatial Data Services keyword | [Keyword node](./keyword-node.md) | |
| 17     | Additional keywords | [Keyword list](./keywordlist.md) | |
| 18     | MD keywords | [Keyword node](./keyword-node.md) | |
| 19     | Geographic Bounding Box | [EX_geographicboundingbox node](ex_geographicboundingbox node.md) | |
| 20     | Temporal reference dates | [Date type](./date-type.md) | |
| 21     | TemporalReference element | [Temporal reference](./temporal-reference.md) | |
| 22     | Degree of conformity | [Degree of conformity](./degree-of-conformity.md) | |
| 23     | Conformity | [Degree of conformity](./degree-of-conformity.md) | |
| 24     | Conditions of access and use  | [Fees node](./fees-node.md) | |
| 25     | Responsible party |  [Contact persone](./contact-person.md) | |
| 26     | Responsible party role | [Contact position](./contact-position.md) | |
| 27     | Point of contact with name and email | [Point of contact details](./point-of-contact-details.md) | |
| 28     | Point of contact in ext. capabilities | [Point of contact details](./point-of-contact-details.md) | |
| 29     | Metadata date | [Metadata date](./metadata-date.md) | |
| 30     | GetCapabilities operation | [Schema validation](./schema-validation.md) | |
| 30     | GetMap Operation | [Getmap format](./getmap-format.md) | |
| 31     | Supported image formats for GetMap | [PNG-GIF image format](./png-gif-image-format.md) | |
| 32     | Layer metadata | [Title and Abstract](./title-and-abstract.md), [keywordlist](./keywordlist.md), [Bounding box in layer](./bbox-in-layer.md), [layer identifier node](./layer-identifier-node.md), [harmonised layer name](./harmonised-layer-name.md), [etrs89 or itrs crs](./etrs89-or-itrs-crs.md), [inspire default styles](./inspire-default-styles.md) | |
| 33     | Layer contains title (wms) | [layer title](./layer-title.md) | |
| 34     | Abstract to describe layer (wms) | [layer language](./layer-language.md) | |
| 35     | Additional layer keywords | [Keywordlist](./keywordlist.md) | |
| 36     | Geographic Bounding Box for WMS | [Minimum geographic bbox](./minimum-geographic-bbox.md) | IR Annex III, Part A, Chapter 2.2.4 |
| 37     | Unique Resource Identifier (layer origin) | [layer identifier node](./layer-identifier-node.md) | |
| 38     | AuthorityURL & Identifier | [Layer identifier node](./layer-identifier-node.md) | |
| 39     | Layer name | [Harmonised layer name](./harmonised-layer-name.md) | IR IOP Article 14 |
| 40     | Coordinate Reference Systems | [etrs89 or itrs crs](./etrs89-or-itrs-crs.md) | |
| 41     | Layer style contains title and identifier | [Layer style name](./layer-style-name.md) | IR Annex III, Part A, Chapter 2.2.4 |
| 42     | inspire_common:default style | [Inspire default styles](./inspire-default-styles.md) | |
| 43     | GCM fallback style | [Review default styles](./review-default-style.md) | |
| 44     | inspire_common:default is the default layer Style | [Review default styles](./review-default-style.md) | |
| 45     | A legend is provided for layers |[Data visualization legend layer](./data-visualization-legend-layer.md)  | |
| 46     | Layer style are mapped correctly (wms) | [layer style name](./layer-style-name.md) | IR Annex III, Part A, Chapter 2.2.4 |
| 47     | Internationalized layer legends | [Data visualization legend layer](./data-visualization-legend-layer.md)  | |
| 48     | Layer Dimension elements | [Dimension](./dimension.md) | |
| 49     | Category layers | [Category Layers.md](./category-layers.md) | |
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
| 60     | Link View Service: scoping | [View service metadata published in an INSPIRE discovery service](./in-discovery-service.md) | |
| 61     | Service metadata in Discovery Service |  [View service metadata published in an INSPIRE discovery service](./in-discovery-service.md) | |
| 62     | Cascading layers in collated capabilities | [Review cascading view services](./cascading-view-services.md) | |
| 63     | Cascaded layers to include "cascaded" attribute | [Review cascading view services](./cascading-view-services.md) | |
| 64     | The value of the "cascaded" attribute indicates cascading level | [Review cascading view services](./cascading-view-services.md) | |
| 65     | Transparency & background for collated layers | [Review cascading view services](./cascading-view-services.md) | |
| 66     | Supported languages | [Supported and response languages node](./supported-and-response-languages-node.md) | IR Annex III, Part A, Chapter 2.2.3 |
| 67     | Client may select the language | [Language selection capabilities](./language-selection-capabilities.md) | |
| 68     | GetCapabilities: LANGUAGE parameter | [Default language](./default-language.md) | |
| 69     | GetCapabilities: default language | [Default language](./default-language.md) | |
| 70     | ResponseLanguage element | [Default language](./default-language.md) | [IR NS](#ref_IR_NS), Annex III, Chapter 2.2.3 |
| 71     | SupportedLanguages and DefaultLanguage elements | [Default language](./default-language.md) | [IR NS](#ref_IR_NS), Annex III, Chapter 2.2.3 |
| 72     | ExtendedCapabilities XML Schema | [Extended capabilities](./extended-capabilities.md) | |
| 73     | GetMap: Portrayal requiring localized rendering | [Default language](./default-language.md) | |

Note: Requirements marked as "not testable" should be reconsidered in a revision of the technical guidance" 

## Two scenarios for providing the service metadata <a name="scenarios"></a>

The [TG VS](#ref_TG_VS) gives two options (scenarios) for providing the service metadata in the Capabilities document of the WMS services:

1. INSPIRE network service metadata in a Discovery Service is referenced through an extended capability.
2. Use (extended) capabilities to map all INSPIRE metadata elements to the WMS 1.3.0 elements.

The requirements considering including the mandatory INSPIRE metadata elements on the Capabilities document depends on which scenario the data provider has chosen to follow. Since there is no dedicated method in [TG VS](#ref_TG_VS) for the data provider to indicate which scenario has been chosen, the validator software must use the following logic to decide the appropriate set of tests to apply:

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

The case of scenario 1, the metadata record referred to by the `inspire_common:MetadataUrl` element must also pass the service scenario of the test suite [ATS Metadata](http://inspire.ec.europa.eu/id/ats/metadata/3.1).

## Tests

This Conformance Class contains the following tests. The "scenario" column of the test table below indicates if the tests are to be applied in service metadata validation scenarios 1, 2 or all (see above).

The tests with a prefix "WMS" refer to the ATS included in the [OGC WMS 1.3.0 specification](#ref_WMS) (Annex A).

| Identifier                                                                          | Scenario(s) | Status   |
| ----------------------------------------------------------------------------------- | -------- | -------- |
| WMS.A.1.2.1 Version negotiation | all | final |
| WMS.A.1.2.2 Request parameter rules | all | final |
| WMS.A.1.2.3 GetCapabilities response | all | final |
| WMS.A.1.2.4 GetMap response | all | final |
| [Bounding box in layer](./bbox-in-layer.md) | all | ready for review |
| [Category layers](./category-layers.md) | all | ready for review |
| [Contact person](./contact-person.md) | all | ready for review |
| [Contact position](./contact-position.md) | all | ready for review |
| [Data visualization legend layer](./data-visualization-legend-layer.md) | Ready for review |
| [Date type](./date-type.md) | 2 only | ready for review |
| [Default language](./default-language.md) | all | ready for review |
| [Degree of conformity](./degree-of-conformity.md) | 2 only | ready for review |
| [ETRS89 or ITRS CRS](./etrs89-or-itrs-crs.md) | all | ready for review |
| [Extended Capabilities](./extended-capabilities.md) | Ready for review |
| [Fees node](./fees-node.md) | all | ready for review |
| [Geographic bounding box](./geographic-bounding-box.md) | all | ready for review |
| [GetMap format](./getmap-format.md) | all | ready for review |
| [Harmonised layer name](./harmonised-layer-name.md) | Ready for review |
| [INSPIRE default styles](./inspire-default-styles.md) | all | ready for review |
| [Keyword node](./keyword-node.md) | 2 only | ready for review |
| [Keyword list](./keywordlist.md) | all | ready for review |
| [Language selection capabilities](./language-selection-capabilities.md) | all | ready for review |
| [Layer identifier node](./layer-identifier-node.md) | all | ready for review |
| [Layer language](./layer-language.md) | Ready for review |
| [Layer style name](./layer-style-name.md) | Ready for review |
| [Layer title](./layer-title.md) | Ready for review |
| [Map coupled resource metadata](./map-coupled-resource-metadata.md) | all | ready for review |
| [Map SDS type with ExtendedCapabilities](./map-sds-type-with-extendedcapabilities.md) | 2 only | ready for review |
| [Metadata date](./metadata-date.md) | 2 only | ready for review |
| [MetadataURL reference INSPIRE service metadata](./metadataurl-reference-inspire-service-metadata.md) | 1 only | ready for review |
| [Minimum geographic bbox](./minimum-geographic-bbox.md) | Ready for review |
| [PNG-GIF image format](./png-gif-image-format.md) | Ready for review |
| [Point-of-contact details](./point-of-contact-details.md) | 2 only | ready for review |
| [Resource locator](./resource-locator.md) | 2 only | ready for review |
| [Resource type is service](./resource-type-is-service.md) | 2 only | ready for review |
| [Review cascading view services](./cascading-view-services.md) | all | ready for review |
| [Review default styles](./review-default-style.md) | all | ready for review |
| [Select language capabilities](./select-language-capabilities.md) | Ready for review |
| [Schema validation](./schema-validation.md) | all | ready for review |
| [Supported and response languages node](./supported-and-response-languages-node.md) | all | ready for review |
| [Temporal reference](./temporal-reference.md) | 2 only | ready for review |
| [Title and abstract](./title-and-abstract.md) | all | ready for review |
| [View service metadata published in an INSPIRE discovery service](./in-discovery-service.md) | all | ready for review |

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
