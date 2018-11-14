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

| Req#   | Description                          | Covered by test(s)                 | 
| ------ | ------------------------------------ | ---------------------------------- | 
| 1      | Scoping: ISO 19128 + INSPIRE ext.    | n/a                                |
| 2      | WMS basic conformance class          | OGC WMS 1.3.0. A.1.2 Basic WMS Server |
| 3      | GetCapabilities, GetMap              | OGC WMS 1.3.0. "WMS basic" CC ATS  |
| 4      | XML schema validation | [at04-getcapabilities-xml-schema-validation](./at04-getcapabilities-xml-schema-validation.md) |
| 5      | GetCapabilities request parameters | [at05-getcapabilities-get-capabilities-request-parameter](./at05-getcapabilities-get-capabilities-request-parameter.md) |
| 6      | MetadataURL references INSPIRE service metadata | [at06-getcapabilities-metadataurl-references-inspire-service-metadata](./at06-getcapabilities-metadataurl-references-inspire-service-metadata.md) |
| 7      | Use WMS and INSPIRE extended capabilities | [at07-getcapabilities-use-wms-inspire-extended-capabilities](./at07-getcapabilities-use-wms-inspire-extended-capabilities.md) |
| 8      | Language section in Extended Capabilities | [at08-getcapabilities-language-section-in-extended-capabilities](./at08-getcapabilities-language-section-in-extended-capabilities.md) |
| 9      | View Service Metadata in Discovery Service | [at09-getcapabilities-view-service-metadata-in-dicovery-service](./at09-getcapabilities-view-service-metadata-in-dicovery-service.md) |
| 10     | Mapping of service metadata elements | [at10-getcapabilities-title-and-abstract](./at10-getcapabilities-title-and-abstract.md) |
| 11     | Resource type is service | [at11-getcapabilities-resource-type-is-service](./at11-getcapabilities-resource-type-is-service.md) |
| 12     | Resource locator | [at12-getcapabilities-resource-locator](./at12-getcapabilities-resource-locator.md) |
| 13     | Map Coupled Resource metadata | [at13-getcapabilities-map-coupled-resource-metadata](./at13-getcapabilities-map-coupled-resource-metadata.md) |
| 14     | Map Coupled Resource metadata URL | [at14-getcapabilities-map-coupled-resource-metadata-url](./at14-getcapabilities-map-coupled-resource-metadata-url.md) |
| 15     | Map SDS Type with Extended Capabilities | [at15-getcapabilities-map-sds-type-with-extendedcapabilities](./at15-getcapabilities-map-sds-type-with-extendedcapabilities.md) |
| 16     | Keyword Node | [at16-getcapabilities-keyword-node](./at16-getcapabilities-keyword-node.md) |
| 17     | Keyword List | [at17-getcapabilities-keyword-list](./at17-getcapabilities-keyword-list.md) |
| 18     | Keyword within ExtendedCapabilities | [at18-getcapabilities-keyword-in-extendedcapabilities](./at18-getcapabilities-keyword-in-extendedcapabilities.md) |
| 19     | Geographic BoundingBox | [at19-getcapabilities-geographic-boundingbox](./at19-getcapabilities-geographic-boundingbox.md) |
| 20     | Date type | [at20-getcapabilities-date-type](./at20-getcapabilities-date-type.md) |
| 21     | Temporal reference | [at21-getcapabilities-temporal-reference](./at21-getcapabilities-temporal-reference.md) |
| 22     | Degree of conformity | [at22-getcapabilities-degree-of-conformity](./at22-getcapabilities-degree-of-conformity.md) |
| 23     | Conformity | [at23-getcapabilities-conformity](./at23-getcapabilities-conformity.md) |
| 24     | Fees node | [at24-getcapabilities-fees-node](./at24-getcapabilities-fees-node.md) |
| 25     | Contanct Organization | [at25-getcapabilities-contact-organization](./at25-getcapabilities-contact-organization.md) |
| 26     | Contact Position | [at26-getcapabilities-contact-position](./at26-getcapabilities-contact-position.md) |
| 27     | Point of Contact | [at27-getcapabilities-point-of-contact](./at27-getcapabilities-point-of-contact.md) |
| 28     | Point of Contact in Extended Capabilities | [at28-getcapabilities-point-of-contact-in-extendedcapabilities](./at28-getcapabilities-point-of-contact-in-extendedcapabilities.md) |
| 29     | Metadata Date | [at29-getcapabilities-metadata-date](./at29-getcapabilities-metadata-date.md) |
| 30     | GetCapabilities Operation Metadata | [at30-getcapabilities-getcapabilities-operation-metadata](./at30-getcapabilities-getcapabilities-operation-metadata.md) |
| 31     | GetMap Operation Metadata | [at31-getcapabilities-get-map-operation-metadata](./at31-getcapabilities-get-map-operation-metadata.md) |
| 32     | Layers Metadata | [at32-getcapabilities-layers-metadata](./at32-getcapabilities-layers-metadata.md) |
| 33     | Layer Title | [at33-getcapabilities-layer-title](./at33-getcapabilities-layer-title.md) |
| 34     | Layer Abstract | [at34-getcapabilities-layer-abstract](./at34-getcapabilities-layer-abstract.md) |
| 35     | Layer Keyword | [at35-getcapabilities-layer-keyword](./at35-getcapabilities-layer-keyword.md) |
| 36     | Layer Geographic Bounding Box | [at36-getcapabilities-layer-bounding-box](./at36-getcapabilities-layer-bounding-box.md) |
| 37     | Layer Unique Resource Identifier | [at37-getcapabilities-layer-unique-resource-identifier](./at37-getcapabilities-layer-unique-resource-identifier.md) |
| 38     | Layer Authority URL | [at38-getcapabilities-layer-authority-url](./at38-getcapabilities-layer-authority-url.md) |
| 39     | Layer Name | [at39-getcapabilities-layer-name](./at39-getcapabilities-layer-name.md) |
| 40     | Layer Coordinate Reference System | [at40-getcapabilities-layer-crs](./at40-getcapabilities-layer-crs.md) |
| 41     | Layer Style | [at41-getcapabilities-layer-style](./at41-getcapabilities-layer-style.md) |
| 42     | Layer Default Style | [at42-getcapabilities-layer-default-style](./at42-getcapabilities-layer-default-style.md) |
| 43     | Layer Simple Style | [at43-getcapabilities-layer-simple-style](./at43-getcapabilities-layer-simple-style.md) |
| 44     | Layer Use Default Style | [at44-getcapabilities-layer-use-default-style](./at44-getcapabilities-layer-use-default-style-title-and-name.md) |
| 45     | Layer Style Legend | [at45-getcapabilities-layer-style-legend](./at45-getcapabilities-layer-style-legend.md) |
| 46     | Layer Style Title and Name | [at46-getcapabilities-layer-style-title-and-name](./at46-getcapabilities-layer-style.md) |
| 47     | Layer Style Legend URL | [at47-getcapabilities-layer-style-legend-url](./at47-getcapabilities-layer-style-legend-url.md) |
| 48     | Layer Dimension Pairs | [at48-getcapabilities-layer-dimension-pairs](./at48-getcapabilities-layer-dimension-pairs.md) |
| 49     | Layer Category Layer | [at49-getcapabilities-layer-category-layer](./at49-getcapabilities-layer-category-layer.md) |
| 50     | GetMap Version Parameter | [at50-getmap-version-parameter](./at50-getmap-version-parameter.md) |
| 51     | GetMap Request Parameter | [at51-getmap-request-parameter](./at51-getmap-request-parameter.md) |
| 52     | GetMap Layers Parameter | [at52-getmap-layers-parameter](./at52-getmap-layers-parameter.md) |
| 53     | GetMap Styles Parameter | [at53-getmap-styles-parameter](./at53-getmap-styles-parameter.md) |
| 54     | GetMap CRS Parameter | [at54-getmap-crs-parameter](./at54-getmap-crs-parameter.md) |
| 55     | GetMap BBOX Parameter | [at55-getmap-bbox-parameter](./at55-getmap-bbox-parameter.md) |
| 56     | GetMap Width and Height Parameter | [at56-getmap-width-height-parameter](./at56-getmap-width-height-parameter.md) |
| 57     | GetMap Format Parameter | [at57-getmap-format-parameter](./at57-getmap-format-parameter.md) |
| 58     | GetMap Transparent Parameter | [at58-getmap-transparent-parameter](./at58-getmap-transparent-parameter.md) |
| 59     | GetMap Exceptions | [at59-getmap-exceptions](./at59-getmap-exceptions.md) |
| 60     | LinkViewService Provide Information | [at60-linkviewservice-provide-information](./at60-linkviewservice-provide-information.md) |
| 61     | LinkViewService Discover | [at61-linkviewservice-discover](./at61-linkviewservice-discover.md) |
| 62     | LinkViewService Layer Metadata | [at62-linkviewservice-layer-metadata](./at62-linkviewservice-layer-metadata.md) |
| 63     | LinkViewService Cascaded Attribute | [at63-linkviewservice-cascaded-attribute](./at63-linkviewservice-cascaded-attribute.md) |
| 64     | LinkViewService Cascaded Increment | [at64-linkviewservice-cascaded-increment](./at64-linkviewservice-cascaded-increment.md) |
| 65     | LinkViewService Transparent BGColor | [at65-linkviewservice-transparent-bgcolor](./at65-linkviewservice-transparent-bgcolor.md) |
| 66     | Language List | [at66-language-list](./at66-language-list.md) |
| 67     | Language Request | [at67-language-request](./at67-language-request.md) |
| 68     | Language Parameter | [at68-language-parameter](./at68-language-parameter.md) |
| 69     | Language Default | [at69-language-default](./at69-language-default.md) |
| 70     | Language Response | [at70-language-response](./at70-language-response.md) |
| 71     | Language Supported | [at71-language-supported](./at71-language-supported.md) |
| 72     | Language Extended Capabilities | [at72-language-extended-capabilities](./at72-language-extended-capabilities.md) |
| 73     | Language Rendered Text | [at73-language-rendered-text](./at73-language-rendered-text.md) |

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

| Identifier                                                                          | Scenario(s) | Type   | Status   |
| ----------------------------------------------------------------------------------- | -------- | -------- |  -------- |
| [at04-getcapabilities-xml-schema-validation](./at04-getcapabilities-xml-schema-validation.md) | all | Automated | ready for review |
| [at05-getcapabilities-get-capabilities-request-parameter](./at05-getcapabilities-get-capabilities-request-parameter.md) | all | Automated | ready for review |
| [at06-getcapabilities-metadataurl-references-inspire-service-metadata](./at06-getcapabilities-metadataurl-references-inspire-service-metadata.md) | 1 only | Automated | ready for review |
| [at07-getcapabilities-use-wms-inspire-extended-capabilities](./at07-getcapabilities-use-wms-inspire-extended-capabilities.md) | 2 only | None | ready for review |
| [at08-getcapabilities-language-section-in-extended-capabilities](./at08-getcapabilities-language-section-in-extended-capabilities.md) | all | Automated | ready for review |
| [at09-getcapabilities-view-service-metadata-in-dicovery-service](./at09-getcapabilities-view-service-metadata-in-dicovery-service.md) | all | Automated | ready for review |
| [at10-getcapabilities-title-and-abstract](./at10-getcapabilities-title-and-abstract.md) | all | Automated | ready for review |
| [at11-getcapabilities-resource-type-is-service](./at11-getcapabilities-resource-type-is-service.md) | 2 only | Automated | ready for review |
| [at12-getcapabilities-resource-locator](./at12-getcapabilities-resource-locator.md) | 2 only | Automated | ready for review |
| [at13-getcapabilities-map-coupled-resource-metadata](./at13-getcapabilities-map-coupled-resource-metadata.md) | all | None | ready for review |
| [at14-getcapabilities-map-coupled-resource-metadata-url](./at14-getcapabilities-map-coupled-resource-metadata-url.md) | all | Automated | ready for review |
| [at15-getcapabilities-map-sds-type-with-extendedcapabilities](./at15-getcapabilities-map-sds-type-with-extendedcapabilities.md) | 2 only | Automated | ready for review |
| [at16-getcapabilities-keyword-node](./at16-getcapabilities-keyword-node.md) | 2 only | Automated | ready for review |
| [at17-getcapabilities-keyword-list](./at17-getcapabilities-keyword-list.md) | 2 only | Automated | ready for review |
| [at18-getcapabilities-keyword-in-extendedcapabilities](./at18-getcapabilities-keyword-in-extendedcapabilities.md) | 2 only | Automated | ready for review |
| [at19-getcapabilities-geographic-boundingbox](./at19-getcapabilities-geographic-boundingbox.md) | 2 only | Automated | ready for review |
| [at20-getcapabilities-date-type](./at20-getcapabilities-date-type.md) | 2 only | Automated | ready for review |
| [at21-getcapabilities-temporal-reference](./at21-getcapabilities-temporal-reference.md) | 2 only | Automated | ready for review |
| [at22-getcapabilities-degree-of-conformity](./at22-getcapabilities-degree-of-conformity.md) | 2 only | Automated | ready for review |
| [at23-getcapabilities-conformity](./at23-getcapabilities-conformity.md) | 2 only | Automated | ready for review |
| [at24-getcapabilities-fees-node](./at24-getcapabilities-fees-node.md) | 2 only | Automated | ready for review |
| [at25-getcapabilities-contact-organization](./at25-getcapabilities-contact-organization.md) | 2 only | Automated | ready for review |
| [at26-getcapabilities-contact-position](./at26-getcapabilities-contact-position.md) | 2 only | Automated | ready for review |
| [at27-getcapabilities-point-of-contact](./at27-getcapabilities-point-of-contact.md) | 2 only | Automated | ready for review |
| [at28-getcapabilities-point-of-contact-in-extendedcapabilities](./at28-getcapabilities-point-of-contact-in-extendedcapabilities.md) | 2 only | Automated | ready for review |
| [at29-getcapabilities-metadata-date](./at29-getcapabilities-metadata-date.md) | 2 only | Automated | ready for review |
| [at30-getcapabilities-getcapabilities-operation-metadata](./at30-getcapabilities-getcapabilities-operation-metadata.md) | all | Automated | ready for review |
| [at31-getcapabilities-get-map-operation-metadata](./at31-getcapabilities-get-map-operation-metadata.md) | all | Automated | ready for review |
| [at32-getcapabilities-layers-metadata](./at32-getcapabilities-layers-metadata.md) | all | None | ready for review |
| [at33-getcapabilities-layer-title](./at33-getcapabilities-layer-title.md) | all | Automated | ready for review |
| [at34-getcapabilities-layer-abstract](./at34-getcapabilities-layer-abstract.md) | all | Automated | ready for review |
| [at35-getcapabilities-layer-keyword](./at35-getcapabilities-layer-keyword.md) | all | Automated | ready for review |
| [at36-getcapabilities-layer-bounding-box](./at36-getcapabilities-layer-bounding-box.md) | all | Automated | ready for review |
| [at37-getcapabilities-layer-unique-resource-identifier](./at37-getcapabilities-layer-unique-resource-identifier.md) | all | None | ready for review |
| [at38-getcapabilities-layer-authority-url](./at38-getcapabilities-layer-authority-url.md) | all | Automated | ready for review |
| [at39-getcapabilities-layer-name](./at39-getcapabilities-layer-name.md) | all | Automated | ready for review |
| [at40-getcapabilities-layer-crs](./at40-getcapabilities-layer-crs.md) | all | Automated | ready for review |
| [at41-getcapabilities-layer-style](./at41-getcapabilities-layer-style.md) | all | None | ready for review |
| [at42-getcapabilities-layer-default-style](./at42-getcapabilities-layer-default-style.md) | all | Automated | ready for review |
| [at43-getcapabilities-layer-simple-style](./at43-getcapabilities-layer-simple-style.md) | all | Manual | ready for review |
| [at44-getcapabilities-layer-use-default-style](./at44-getcapabilities-layer-use-default-style.md) | all | Manual | ready for review |
| [at45-getcapabilities-layer-style-legend](./at45-getcapabilities-layer-style-legend.md) | all | None | ready for review |
| [at46-getcapabilities-layer-style-title-and-name](./at46-getcapabilities-layer-style.md) | all | Automated | ready for review |
| [at47-getcapabilities-layer-style-legend-url](./at47-getcapabilities-layer-style-legend-url.md) | all | Automated | ready for review |
| [at48-getcapabilities-layer-dimension-pairs](./at48-getcapabilities-layer-dimension-pairs.md) | all | Automated | ready for review |
| [at49-getcapabilities-layer-category-layer](./at49-getcapabilities-layer-category-layer.md) | all | Automated | ready for review |
| [at50-getmap-version-parameter](./at50-getmap-version-parameter.md) | all | Automated | ready for review |
| [at51-getmap-request-parameter](./at51-getmap-request-parameter.md) | all | Automated | ready for review |
| [at52-getmap-layers-parameter](./at52-getmap-layers-parameter.md) | all | Automated | ready for review |
| [at53-getmap-styles-parameter](./at53-getmap-styles-parameter.md) | all | Automated | ready for review |
| [at54-getmap-crs-parameter](./at54-getmap-crs-parameter.md) | all | Automated | ready for review |
| [at55-getmap-bbox-parameter](./at55-getmap-bbox-parameter.md) | all | Automated | ready for review |
| [at56-getmap-width-height-parameter](./at56-getmap-width-height-parameter.md) | all | Automated | ready for review |
| [at57-getmap-format-parameter](./at57-getmap-format-parameter.md) | all | Automated | ready for review |
| [at58-getmap-transparent-parameter](./at58-getmap-transparent-parameter.md) | all | Automated | ready for review |
| [at59-getmap-exceptions](./at59-getmap-exceptions.md) | all | Automated | ready for review |
| [at60-linkviewservice-provide-information](./at60-linkviewservice-provide-information.md) | all | None | ready for review |
| [at61-linkviewservice-discover](./at61-linkviewservice-discover.md) | all | Automated | ready for review |
| [at62-linkviewservice-layer-metadata](./at62-linkviewservice-layer-metadata.md) | all | Automated | ready for review |
| [at63-linkviewservice-cascaded-attribute](./at63-linkviewservice-cascaded-attribute.md) | all | Automated | ready for review |
| [at64-linkviewservice-cascaded-increment](./at64-linkviewservice-cascaded-increment.md) | all | Automated | ready for review |
| [at65-linkviewservice-transparent-bgcolor](./at65-linkviewservice-transparent-bgcolor.md) | all | Automated | ready for review |
| [at66-language-list](./at66-language-list.md) | all | None | ready for review |
| [at67-language-request](./at67-language-request.md) | all | None | ready for review |
| [at68-language-parameter](./at68-language-parameter.md) | all | Automated | ready for review |
| [at69-language-default](./at69-language-default.md) | all | Automated | ready for review |
| [at70-language-response](./at70-language-response.md) | all | Automated | ready for review |
| [at71-language-supported](./at71-language-supported.md) | all | Automated | ready for review |
| [at72-language-extended-capabilities](./at72-language-extended-capabilities.md) | all | Automated | ready for review |
| [at73-language-rendered-text](./at73-language-rendered-text.md) | all | None | ready for review |

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
