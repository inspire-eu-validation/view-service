ats-view-wms
============

Abstract Test Suite for INSPIRE View Services Technical Guidance ISO 19128 Profile (OGC Web Map Service 1.3.0)

*Note*: This ATS is in Ready for review stage, none of the tests have an official INSPIRE MIG approval.

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
| 2      | WMS basic conformance class          | OGC WMS 1.3.0. A.1.2 Basic WMS Server, [A.03.IR05.schema.validation](A.03.IR05.schema.validation.md)  | n/a  |
| 3      | GetCapabilities, GetMap              | OGC WMS 1.3.0. "WMS basic" CC ATS  | n/a |
| 4      | INSPIRE ExtendedCapabilities         | [A.02.IR04.extended.capabilities.node](A.02.IR04.extended.capabilities.node.md) | n/a |
| 5      | GetCapabilities request parameters   | OGC WMS 1.3.0. "WMS basic" CC ATS,  | [IR NS](#ref_IR_NS), Annex III, Chapter 2.1.1 |
| 6      | INSPIRE MetadataURL element | [A.04.IR06.metadataURL.node](A.04.IR06.metadataURL.node.md) | |
| 7      | Use WMS + INSPIRE extended capabilities  | Test bound to specific requirements | n/a |
| 8      | Language section in Extended capabilities | [A.06.IR08.language.node](A.06.IR08.language.node.md) | [IR NS](#ref_IR_NS), Annex III, Chapter 2.2.3 |
| 9      | View Service Metadata in Discovery Service | Not testable |  [IR NS](#ref_IR_NS), Annex III, Chapter 4. |
| 10     | Mapping of service metadata elements | [A.05](A.05.extended.capabilities.elements.node.md), [A.07](A.07.IR10.title.abstract.md), [A.08](A.08.IR11.resource.type.node.md), [A.09](A.09.IR12.resource.locator.node.md), [A.10](A.10.IR12.coupled.resource.node.md), [A.11](A.11.IR14.metadata.record.node.md), [A.12](A.12.IR15.spatialdataservicetype.node.md), [A.13](A.13.IR18.keywords.node.md), [A.14](A.14.IR19.geographicboundingbox.node.md), [A.15](A.15.IR20.dates.node.md), [A.16](A.16.IR21.temporal.reference.node.md), [A.17](A.17.IR22.conformity.degree.node.md), [A.18](A.18.IR23.conformity.node.md), [A.19](A.19.IR24.fees.node.md), [A.20](A.20.IR25.contactpersonprimary.node.md), [A.21](A.21.IR26.contactposition.node.md), [A.22](A.22.IR27.IR28.metadata.pointofcontact.node.md), [A.24](A.24.IR29.metadata.date.node.md) | [IR MD](#ref_IR_MD), Part B |
| 11     | ResourceType element | [A.08.IR11.resource.type.node](A.08.IR11.resource.type.node.md) | |
| 12     | ResourceLocator element | [A.09.IR12.resource.locator.node](A.09.IR12.resource.locator.node.md) | |
| 13     | MetadataURL for each layer | [A.10.IR13.coupled.resource.node](A.10.IR13.coupled.resource.node.md) | |
| 14     | MetadataURL resolvable to MD record | [A.11.IR14.metadata.record.node](A.11.IR14.metadata.record.node.md) | |
| 15     | SpatialDataServiceType element | [A.12.IR15.spatialdataservicetype.node](A.12.IR15.spatialdataservicetype.node.md) | |
| 16     | Classification of Spatial Data Services keyword | [A.39.IR16.spatial.data.service.keyword.embedded.metadata](A.39.IR16.spatial.data.service.keyword.embedded.metadata.md) | |
| 17     | Additional keywords | Not testable | |
| 18     | MD keywords | [A.13.IR18.keywords.node](A.13.IR18.keywords.node.md) | |
| 19     | Geographic Bounding Box | [A.14.IR19.geographicboundingbox.node](A.14.IR19.geographicboundingbox.node.md) | |
| 20     | Temporal reference dates | [A.15.IR20.dates.node](A.15.IR20.dates.node.md) | |
| 21     | TemporalReference element | [A.16.IR21.temporal.reference.node](A.16.IR21.temporal.reference.node.md) | |
| 22     | Degree of conformity | [A.17.IR22.conformity.degree.node](A.17.IR22.conformity.degree.node.md) | |
| 23     | Conformity | [A.18.IR23.conformity.node](A.18.IR23.conformity.node.md) | |
| 24     | Conditions of access and use  | [A.19.IR24.fees.node](A.19.IR24.fees.node.md) | |
| 25     | Responsible party |  [A.20.IR25.contactpersonprimary.node](A.20.IR25.contactpersonprimary.node.md) | |
| 26     | Responsible party role | [A.21.IR26.contactposition.node](A.21.IR26.contactposition.node.md) | |
| 27     | Point of contact with name and email | [A.22.IR27.IR28.metadata.pointofcontact.node](A.22.IR27.IR28.metadata.pointofcontact.node.md) | |
| 28     | Point of contact in ext. capabilities | [A.22.IR27.IR28.metadata.pointofcontact.node](A.22.IR27.IR28.metadata.pointofcontact.node.md) | |
| 29     | Metadata date | [A.24.IR29.metadata.date.node](A.24.IR29.metadata.date.node.md) | |
| 30     | GetCapabilities operation | [A.03.IR05.schema.validation](A.03.IR05.schema.validation.md) | |
| 31     | GetMap with PNG of GIF | [A.26.IR31.getmap.format.node](A.26.IR31.getmap.format.node.md) | |
| 32     | Layer metadata | [A.28](A.28.IR33.layer.title.node.md), [A.29](A.29.IR34.layer.abstract.node.md), [A.30](A.30.IR35.layer.keywordlist.node.md), [A.31](A.31.IR36.layer.bbox.node.md), [A.32](A.32.IR38.layer.identifier.node.md), [A.33](A.33.IR38.layer.authority.url.node.md), [A.34](A.34.IR46.style.node.md), [A.35](A.35.IR39.harmonized.layer.name.md), [A.36](A.36.IR40.etrs89.irts.crs.md), [A.37](A.37.IR42.inspire.default.style.md), [A.38](A.38.IR45.IR47.style.legend.url.md) | |
| 33     | Harmonised layer title | [A.28.IR33.layer.title.node](A.28.IR33.layer.title.node.md) | |
| 34     | Layer abstract | [A.29.IR34.layer.abstract.node](A.29.IR34.layer.abstract.node.md) | |
| 35     | Additional layer keywords | [A.30.IR35.layer.keywordlist.node](A.30.IR35.layer.keywordlist.node.md) | |
| 36     | Layer Bounding Box | [A.31.IR36.layer.bbox.node](A.31.IR36.layer.bbox.node.md) | |
| 37     | Unique Resource Indentifier (layer origin) | Not testable | |
| 38     | AuthorityURL & Indentifier | [A.32.IR38.layer.identifier.node](A.32.IR38.layer.identifier.node.md), [A.33.IR38.layer.authority.url.node](A.33.IR38.layer.authority.url.node.md) | |
| 39     | Harmonised layer name | [A.35.IR39.harmonised.layer.name](A.35.IR39.harmonised.layer.name.md) | [IR IOP](#ref_IR_IOP), Article 14 |
| 40     | Coordinate Reference Systems | [A.36.IR40.etrs89.irts.crs](A.36.IR40.etrs89.irts.crs.md) | |
| 41     | Style composed of title and identifier | [A.34.IR46.style.node](A.34.IR46.style.node.md) | |
| 42     | inspire_common:default style | [A.37.IR42.inspire.default.style](A.37.IR42.inspire.default.style.md) | |
| 43     | GCM fallback style | Not testable | |
| 44     | inspire_common:default is the default layer Style | Not testable | |
| 45     | Layer legend for each style+language combination | [A.38.IR45.IR47.style.legend.url](A.38.IR45.IR47.style.legend.url.md) | |
| 46     | Style by wms:Style element | [A.34.IR46.style.node](A.34.IR37.style.node.md) | |
| 47     | Layer legend by LegendURL element | [A.38.IR45.IR47.style.legend.url](A.38.IR45.IR47.style.legend.url.md) | |
| 48     | Layer Dimension elements | Not testable | |
| 49     | Category layers | Not testable | |
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
| 60     | Link View Service: scoping | Not testable | |
| 61     | Service metadata in Discovery Service |  Not testable | |
| 62     | Cascading layers in collated capabilities | Not testable | |
| 63     | Cascaded layers to include "cascaded" attribute | Not testable | |
| 64     | The value of the "cascaded" attribute indicates cascading level | Not testable | |
| 65     | Transparency & background for collated layers | Not testable | |
| 66     | List of supported languages | [A.06.IR08.language.node](A.06.IR08.language.node.md) | [IR NS](#ref_IR_NS), Annex III, Chapter 2.2.3 |
| 67     | Client may select the language | [A.40.IR67.IR68.language.affects.capabilities](A.40.IR67.IR68.language.affects.capabilities.md) | |
| 68     | GetCapabilities: LANGUAGE parameter | [A.40.IR67.IR68.language.affects.capabilities](A.40.IR67.IR68.language.affects.capabilities.md) | |
| 69     | GetCapabilities: default language | [A.41.IR69.default.language](A.41.IR69.default.language.md) | |
| 70     | ResponseLanguage element | [A.40.IR67.IR68.language.affects.capabilities](A.40.IR67.IR68.language.affects.capabilities.md) | [IR NS](#ref_IR_NS), Annex III, Chapter 2.2.3 |
| 71     | SupportedLanguages and DefaultLanguage elements | [A.06.IR08.language.node](A.06.IR08.language.node.md) | [IR NS](#ref_IR_NS), Annex III, Chapter 2.2.3 |
| 72     | ExtendedCapabilities XML Schema | [A.02.IR04.extended.capabilities.node](A.02.IR04.extended.capabilities.node.md) | |
| 73     | GetMap: Portrayal requiring localized rendering | Not testable | |

## Two scenarios for providing the service metadata

The [TG VS](#ref_TG_VS) gives two options (scenarios) for providing the service metadata in the Capabilities document of the WMS services:

1. INSPIRE network service metadata in a Discovery Service is referenced through an extended capability.
2. Use (extended) capabilities to map all INSPIRE metadata elements to the WMS 1.3.0 elements.

The requirements considering including the mandatory INSPIRE metadata elements on the Capabilities document depend on which scenario the data provider has chosen to follow. Since there is no dedicated method in [TG VS](#ref_TG_VS) for the data prodiver to
indicate which scenario he/she has chosen, the validator software must use the following logic to decide the appropriate
set of tests to apply:

The scenario 2 is selected only if at least one of the following elements exists in
the WMS Capabilities document's `inspire_vs:ExtendedCapabilities` element:

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

The the case of scenario 1, the the metadata record referred to by the `inspire_common:MetadataUrl` element must also pass the service scenario of the test suite [ats-metadata](https://github.com/inspire-eu-validation/ats-metadata).

## Tests

This Conformance Class contains the following tests. The "scenario" column of the test table below indicates if the tests are to be applied in service metadata validation scenarios 1, 2 or all (see above).

The tests with a prefix "WMS" refer to the ATS included in the [OGC WMS 1.3.0 specification](#ref_WMS) (Annex A).

| Identifier                                                                          | Scenario(s) | Status   |
| ----------------------------------------------------------------------------------- | -------- | -------- |
| WMS.A.1.2.1 Version negotiation | All | Final |
| WMS.A.1.2.2 Request parameter rules | All | Final |
| WMS.A.1.2.3 GetCapabilities response | All | Final |
| WMS.A.1.2.4 GetMap response | All | Final |
| [A.02.IR04.extended.capabilities.node](A.02.IR04.extended.capabilities.node.md) | All | Ready for review |
| [A.03.IR05.schema.validation](A.03.IR05.schema.validation.md) | All | Ready for review |
| [A.04.IR06.metadataURL.node](A.04.IR06.metadataURL.node.md) | 1 only | Ready for review |
| [A.05.IR07.extended.capabilities.elements.node](A.05.extended.capabilities.elements.node.md) | 2 only | Ready for review |
| [A.06.IR08.language.node](A.06.IR08.language.node.md) | All | Ready for review |
| [A.07.IR10.title.abstract](A.07.IR10.title.abstract.md) | All | Ready for review |
| [A.08.IR11.resource.type.node](A.08.IR11.resource.type.node.md) | 2 only | Ready for review |
| [A.09.IR12.resource.locator.node](A.09.IR12.resource.locator.node.md) | 2 only | Ready for review |
| [A.10.IR13.coupled.resource.node](A.10.IR12.coupled.resource.node.md) | All | Ready for review |
| [A.11.IR14.metadata.record.node](A.11.IR14.metadata.record.node.md) | All | Ready for review |
| [A.12.IR15.spatialdataservicetype.node](A.12.IR15.spatialdataservicetype.node.md) | 2 only | Ready for review |
| [A.13.IR18.keywords.node](A.13.IR18.keywords.node.md) | 2 only | Ready for review |
| [A.14.IR19.geographicboundingbox.node](A.14.IR19.geographicboundingbox.node.md) | All | Ready for review |
| [A.15.IR20.dates.node](A.15.IR20.dates.node.md) | 2 only | Ready for review |
| [A.16.IR21.temporal.reference.node](A.16.IR21.temporal.reference.node.md) |  2 only | Ready for review |
| [A.17.IR22.conformity.degree.node](A.17.IR22.conformity.degree.node.md) | 2 only | Ready for review|
| [A.18.IR23.conformity.node](A.18.IR23.conformity.node.md) | 2 only | Ready for review |
| [A.19.IR24.fees.node](A.19.IR24.fees.node.md) | All | Ready for review |
| [A.20.IR25.contactpersonprimary.node](A.20.IR25.contactpersonprimary.node.md) | All | Ready for review |
| [A.21.IR26.contactposition.node](A.21.IR26.contactposition.node.md) | All | Ready for review|
| [A.22.IR27.IR28.metadata.pointofcontact.node](A.22.IR27.IR28.metadata.pointofcontact.node.md) | 2 only | Ready for review |
| [A.24.IR29.metadata.date.node](A.24.IR29.metadata.date.node.md) | 2 only | Ready for review |
| [A.26.IR31.getmap.format.node](A.26.IR31.getmap.format.node.md) | All | Ready for review |
| [A.28.IR33.layer.title.node](A.28.IR33.layer.title.node.md) | All | Ready for review |
| [A.29.IR34.layer.abstract.node](A.29.IR34.layer.abstract.node.md) | All | Ready for review |
| [A.30.IR35.layer.keywordlist.node](A.30.IR35.layer.keywordlist.node.md) | All | Ready for review |
| [A.31.IR36.layer.bbox.node](A.31.IR36.layer.bbox.node.md) | All | Ready for review |
| [A.32.IR38.layer.identifier.node](A.32.IR38.layer.identifier.node.md) | All |Ready for review |
| [A.33.IR38.layer.authority.url.node](A.33.IR38.layer.authority.url.node.md) | All | Ready for review |
| [A.34.IR46.style.node](A.34.IR46.style.node.md) | All | Ready for review |
| [A.35.IR39.harmonised.layer.name](A.35.IR39.harmonised.layer.name.md) | All | Ready for review |
| [A.36.IR40.etrs89.irts.crs](A.36.IR40.etrs89.irts.crs.md) | All | Ready for review |
| [A.37.IR42.inspire.default.style](A.37.IR42.inspire.default.style.md) | All | Ready for review |
| [A.38.IR45.IR47.style.legend.url](A.38.IR45.IR47.style.legend.url.md) | All | Ready for review |
| [A.39.IR16.spatial.data.service.keyword.embedded.metadata](A.39.IR16.spatial.data.service.keyword.embedded.metadata.md) | 2 only | Ready for Review |
| [A.40.IR67.IR68.language.affects.capabilities](A.40.IR67.IR68.language.affects.capabilities.md) | All | Ready for review |
| [A.41.IR69.default.language](A.41.IR69.default.language.md) | All | Ready for review |

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
