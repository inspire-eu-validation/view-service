# Scenario 2 - Mapping of service metadata elements

**Purpose**: Test that the capabilities section of the View Service contains the Service metadata elements in accordance with [Table 3a](#table3a).

**Prerequisites**

This test only applies to [Scenario 2](./README.md#scenarios). Otherwise, the test case is skipped.

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * Check that exactly one [Title](#title) element is provided and it is not empty.

  * Check that exactly one [Abstract](#abstract) element is provided and it is not empty.

  * Check that there is exactly one [Resource Type](#ResourceType) element and its value is 'service'.
  
  * Check that a [Resource Locator](#ResourceLocator) element is provided and the [URL](#ResourceLocatorURL) is working.
  
  * Check that, if there is a [MetadataURL](#metadataURL) element for a layer:

    * the [OnlineResource](#onlineResource) element has an 'xlink:href' attribute, its content is not empty and one of the following checks is passed:

      * a valid response is returned sending a HTTP/GET request to the GetRecorById of the Discovery Service, .

      * a direct link is provided to the ISO19139 metadata document.
      
    * otherwise, check manually that "_if linkage to data sets on which the service operates are available_" the [MetadataURL](#metadataURL) element is mandatory.
  
  * Check that there is a [SpatialDataServiceType](#SpatialDataServiceType) element and that has a fixed value equal to 'view'. 
  
  * Check that at least one [Keyword](#mandatoryKeyword) element with a value from the "[Classification of Spatial data Services](https://inspire.ec.europa.eu/metadata-codelist/SpatialDataServiceCategory)" codelist is provided.

  * Check if there is a [EX_GeographicBoundingBox](#EX_GeographicBoundingBox) element in each named Layer element or if it is inherited from a parent Layer, otherwise:
  
    * check manually that "_if the service has an explicit geographic extent._" the [EX_GeographicBoundingBox](#EX_GeographicBoundingBox) element is mandatory.

  * Check that at least one [DateOfPublication](#DateOfPublication), [DateOfLastRevision](#DateOfLastRevision) or [DateOfCreation](#DateOfCreation) element is provided and that the provided date is formated in YYYY-MM-DD.

  * Check that at least one [Conformity](#Conformity) element is provided with the declaration of conformity against the Commission Regulation (EC) No 976/2009 of 19 October 2009 implementing Directive 2007/2/EC of the European Parliament and of the Council as regards the Network Services - URI: http://data.europa.eu/eli/reg/2009/976. (Regulation name or URI shall be provided in the [Specification Title](#SpecificationTitle).)

  * Check that at least one [Fees](#Fees) element is provided defining the conditions for access and use. If no conditions apply to the access and use of the resource, "no conditions apply" shall be used. If conditions are unknown "conditions unknown" shall be used.

  * Check that at least one [AccessConstraints](#accessConstraints) element is provided.
  
  * Check that the Responsible Organisation is provided through the [ContactOrganization](#ContactOrganization) element and that the Responsible Party role is provided through the [ContactPosition](#ContactPosition) element with one of the values of code list [Responsible party role](https://inspire.ec.europa.eu/metadata-codelist/ResponsiblePartyRole).

  * Check that the Metadata Point of Contact is provided through the [OrganisationName](#OrganisationName) and the [EmailAddress](#EmailAddress) elements of the MetadataPointOfContact element.
  
  * Check that exactly one [MetadataDate](#MetadataDate) element is provided and the date is expressed in conformity with ISO 8601.
  
  * Check that there is a [SupportedLanguages](#SupportedLanguage) element.


Table 3a <a name="table3a"></a>: Mapping between INSPIRE metadata elements and [ISO 19128] WMS elements with the use of extended capabilities.

| INSPIRE Metadata element<br>(***M***andatory - ***C***onditional) | ISO 19128 or<br>INSPIRE ExtendedCapabilities element     | Multiplicity | Condition            | Specific TG requirement (if present)/Notes      | Check type         |
| -------------------------------------- | -------------------------------------------------------------------------------- | ------------ | -------------------- | ----------------------------------------- | ------------------ |
| Resource Title (_M_)                   | wms:Title                                                                        | 1            |                      |                                           | Automatic          |
| Resource Abstract (_M_)                | wms:Abstract                                                                     | 1            |                      |                                           | Automatic          |
| Resource Type (_M_)                    | inspire_common:ResourceType<br>(ExtendedCapabilities)                            | 1            |                      | Requirement 11: the value shall be 'service'.            | Automatic          |
| Resource Locator (_C_)                 | inspire_common:ResourceLocator<br>(ExtendedCapabilities)                         | 0..\*        | Mandatory if linkage to the service is available.   |The element is mandatory in the inspire_vs.xsd              | Automatic |
| Coupled Resource (_C_)                 | wms:MetadataURL<br>(Layer property)                                              | 0..\*        | Mandatory if linkage to data sets on which the service operates are available.    | Requirement 14: the value shall be a URL that allows access to a metadata record.      | Automatic + Manual |
| Spatial Data Service Type (_M_)        | inspire_common:SpatialDataServiceType<br>(ExtendedCapabilities)                  | 1            |      | Requirement 15:  the value shall be 'view'.     | Automatic          |
| Keyword (_M_)                          | wms:Keyword and wms:Keyword/@vocabulary;<br>inspire_common:Keyword               | 1..\*        |       | Requirement 16:  at least one keyword from the Classification of spatial data services shall be provided.      | Automatic          |
| Geographic Bounding Box (_C_)          | wms:EX_GeographicBoundingBox<br>(Layer property)                                 | 0..\*        | Mandatory for services with an explicit geographic extent.                        |     | Automatic + Manual |
| Temporal Reference (_M_)               | inspire_common:TemporalReference<br>(ExtendedCapabilities)                       | 1..\*        |                                                                                   | Requirement 20: one of the following dates shall be provided: date of publication, date of last revision, or the date of creation. Date of last revision is preferred. The date shall be expressed in conformity with ISO 8601. | Automatic          |
| Spatial Resolution (_C_)               | wms:Abstract                                                                     | 0..\*        | Mandatory when there is a restriction on the spatial resolution for this service. |                                                                                                                                                                                                                                 | Manual             |
| Conformity (_M_)                       | inspire_common:Conformity<br>(ExtendedCapabilities)                              | 1..\*        |                                                                                   |                                                                                                                                                                                                                                 | Automatic          |
| Conditions for Access and Use (_M_)    | wms:Fees                                                                         | 1..\*        |                                                                                   | Requirement 24: If no conditions apply to the access and use of the resource, the value "no conditions apply" shall be used. If conditions are unknown "conditions unknown" shall be used.                                      | Automatic          |
| Limitations on Public Access (_M_)     | wms:AccessConstraints                                                            | 1..\*        |                                                                                   |                                                                                                                                                                                                                                 | Automatic          |
| Responsible Organisation (_M_)         | wms:ContactInformation/ wms:ContactPersonPrimary/ wms:ContactOrganization<br>and<br>wms:ContactInformation/ wms:ContactPosition       | 1..\*        |         | Requirement 26: The value domain of the Responsible Party role shall be one of the values of code list Responsible party role.                                                                                                                       | Automatic          |
| Metadata Point of Contact (_M_)        | inspire_common:MetadataPointOfContact<br>(ExtendedCapabilities)                  | 1..\*        |                                                                                   | Requirement 27: The role of the metadata point of contact shall be "pointOfContact".                                                                                                                                            | Automatic          |
| Metadata Date (_M_)                    | inspire_common:MetadataDate<br>(ExtendedCapabilities)                            | 1            |                                                                                   | Requirement 29: The date shall be expressed in conformity with the [INS MD], meaning it shall be expressed in conformity with ISO 8601.                                                                                         | Automatic          |
| Metadata Language (_M_)                | inspire_common:SupportedLanguages<br>(ExtendedCapabilities)                      | 1            |             |                                                                                                                                                                                                                                 | Automatic          |


**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.1, Requirement 6 - Section 2, Requirement 11
* [INS MD](./README.md#ref_INS_MD), Part C - Table 2; Classification of Spatial data Services, Part D.4

**Test type**: Automated

**Notes**

As stated by the INSPIRE Metadata Technical Guidance [INS MDTG], it is not possible to express the restriction of a service concerning the spatial resolution in the current version of [ISO 19119].
While this issue is being addressed by the standardisation community, spatial resolution restrictions for services shall be written in the Abstract as mandated by the Metadata Technical Guidance [INS MDTG]. Spatial Resolution restrictions at service metadata
level shall be declaratively described in the wms:Abstract element.

For the AccessConstraints element, is recomended to use "None" value when any constrainst is applied and when constraints are imposed may be used the codelists defined in [ISO 19115, Annex B – Data Dictionary, Section 5.24].

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).
Related XPaths are provided in the table above.

Abbreviation                                                     |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------------- | -------------------------------------------------------------------------
Resource Title <a name="title"></a>                              | wms:Service/wms:Title
Resource Abstract <a name="abstract"></a>                        | wms:Service/wms:Abstract
Resource Type <a name="ResourceType"></a>                        | wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:ResourceType
Resource Locator <a name="ResourceLocator"></a>                  | wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:ResourceLocator
Resource Locator URL <a name="ResourceLocatorURL"></a>           | wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:ResourceLocator/inspire_common:URL
MetadataURL <a name="metadataURL"></a>                           | wms:Capability/\*/wms:Layer/MetadataURL
OnlineResource <a name="onlineResource"></a>                     | wms:Capability/\*/wms:Layer/MetadataURL/OnlineResource
SpatialDataServiceType <a name="SpatialDataServiceType"></a>     | wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:SpatialDataServiceType
Keyword <a name="mandatoryKeyword"></a>                          | wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:MandatoryKeyword
EX_GeographicBoundingBox <a name="EX_GeographicBoundingBox"></a> | wms:Capability/wms:Layer/wms:EX_GeographicBoundingBox
DateOfPublication <a name="DateOfPublication"></a>               | wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:TemporalReference/inspire_common:DateOfPublication
DateOfLastRevision <a name="DateOfLastRevision"></a>             | wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:TemporalReference/inspire_common:DateOfLastRevision
DateOfCreation <a name="DateOfCreation"></a>                     | wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:TemporalReference/inspire_common:DateOfCreation
Conformity <a name="Conformity"></a>                             | wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:Conformity
Specification Title <a name="SpecificationTitle"></a>            | wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:Conformity/inspire_common:Specification/inspire_common:Title
Fees <a name="Fees"></a>                                         | wms:Service/wms:Fees
Access Constraints <a name="accessConstraints"></a>              | wms:Service/wms:AccessConstraints
ContactOrganization <a name="ContactOrganization"></a>           | wms:Service/wms:ContactInformation/wms:ContactPersonPrimary/wms:ContactOrganization
ContactPosition <a name="ContactPosition"></a>                   | wms:Service/wms:ContactInformation/wms:ContactPosition
OrganisationName <a name="OrganisationName"></a>                 | wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:MetadataPointOfContact/inspire_common:OrganisationName
EmailAddress <a name="EmailAddress"></a>                         | wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:MetadataPointOfContact/inspire_common:EmailAddress
MetadataDate <a name="MetadataDate"></a>                         | wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:MetadataDate
SupportedLanguage <a name="SupportedLanguage"></a>               | wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:SupportedLanguages