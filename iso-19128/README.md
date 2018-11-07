# Conformance class: INSPIRE Profile of ISO 19128 (DRAFT)

This conformance class is part of the [Abstract Test Suite for the INSPIRE View Services Technical Guidance](http://inspire.ec.europa.eu/id/ats/view-service/3.11).

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
| 8      |  | [](./.md) | |
| 9      |  | [](./.md) | |
| 10     |  | [](./.md) | |
| 11     |  | [](./.md) | |
| 12     |  | [](./.md) | |
| 13     |  | [](./.md) | |
| 14     |  | [](./.md) | |
| 15     |  | [](./.md) | |
| 16     |  | [](./.md) | |
| 17     |  | [](./.md) | |
| 18     |  | [](./.md) | |
| 19     |  | [](./.md) | |
| 20     |  | [](./.md) | |
| 21     |  | [](./.md) | |
| 22     |  | [](./.md) | |
| 23     |  | [](./.md) | |
| 24     |  | [](./.md) | |
| 25     |  | [](./.md) | |
| 26     |  | [](./.md) | |
| 27     |  | [](./.md) | |
| 28     |  | [](./.md) | |
| 29     |  | [](./.md) | |
| 30     |  | [](./.md) | |
| 30     |  | [](./.md) | |
| 31     |  | [](./.md) | |
| 32     |  | [](./.md) | |
| 33     |  | [](./.md) | |
| 34     |  | [](./.md) | |
| 35     |  | [](./.md) | |
| 36     |  | [](./.md) | |
| 37     |  | [](./.md) | |
| 38     |  | [](./.md) | |
| 39     |  | [](./.md) | |
| 40     |  | [](./.md) | |
| 41     |  | [](./.md) | |
| 42     |  | [](./.md) | |
| 43     |  | [](./.md) | |
| 44     |  | [](./.md) | |
| 45     |  | [](./.md) | |
| 46     |  | [](./.md) | |
| 47     |  | [](./.md) | |
| 48     |  | [](./.md) | |
| 49     |  | [](./.md) | |
| 50     | GetMap Version Parameter | [at50-getmap-version-parameter](./at50-getmap-version-parameter.md) | |
| 51     | GetMap Request Parameter | [at51-getmap-request-parameter](./at51-getmap-request-parameter.md) | |
| 52     | GetMap Layers Parameter | [at52-getmap-layers-parameter](./at52-getmap-layers-parameter.md) | |
| 53     | GetMap Styles Parameter | [at53-getmap-styles-parameter](./at53-getmap-styles-parameter.md) | |
| 54     | GetMap CRS Parameter | [at54-getmap-crs-parameter](./at54-getmap-crs-parameter.md) | |
| 55     | GetMap BBOX Parameter | [at55-getmap-bbox-parameter](./at55-getmap-bbox-parameter.md) | |
| 56     | GetMap Width and Height Parameter | [at56-getmap-width-height-parameter](./at56-getmap-width-height-parameter.md) | |
| 57     | GetMap Format Parameter | [at57-getmap-format-parameter](./at57-getmap-format-parameter.md) | |
| 58     | GetMap Transparent Parameter | [at58-getmap-transparent-parameter](./at58-getmap-transparent-parameter.md) | |
| 59     | GetMap Exceptions | [at59-getmap-exceptions](./at59-getmap-exceptions.md) | |
| 60     | LinkViewService Provide Information | [at60-linkviewservice-provide-information](./at60-linkviewservice-provide-information.md) | |
| 61     | LinkViewService Discover | [at61-linkviewservice-discover](./at61-linkviewservice-discover.md) | |
| 62     | LinkViewService Layer Metadata | [at62-linkviewservice-layer-metadata](./at62-linkviewservice-layer-metadata.md) | |
| 63     | LinkViewService Cascaded Attribute | [at63-linkviewservice-cascaded-attribute](./at63-linkviewservice-cascaded-attribute.md) | |
| 64     | LinkViewService Cascaded Increment | [at64-linkviewservice-cascaded-increment](./at64-linkviewservice-cascaded-increment.md) | |
| 65     | LinkViewService Transparent BGColor | [at65-linkviewservice-transparent-bgcolor](./at65-linkviewservice-transparent-bgcolor.md) | |
| 66     | Language List | [at66-language-list](./at66-language-list.md) | |
| 67     | Language Request | [at67-language-request](./at67-language-request.md) | |
| 68     | Language Parameter | [at68-language-parameter](./at68-language-parameter.md) | |
| 69     | Language Default | [at69-language-default](./at69-language-default.md) | |
| 70     | Language Response | [at70-language-response](./at70-language-response.md) | [IR NS](#ref_IR_NS), Annex III, Chapter 2.2.3 |
| 71     | Language Supported | [at71-language-supported](./at71-language-supported.md) | [IR NS](#ref_IR_NS), Annex III, Chapter 2.2.3 |
| 72     | Language Extended Capabilities | [language-extended-capabilities](./at72-language-extended-capabilities.md) | |
| 73     | Language Rendered Text | [language-rendered-text](./at73-language-rendered-text.md) | |

Note: Requirements marked as "not testable" should be reconsidered in a revision of the technical guidance" 

## <a name="scenarios"></a> Two scenarios for providing the service metadata

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
