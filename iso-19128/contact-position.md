# Contact position

**Purpose**: The value domain of the Responsible Party role shall comply with the INSPIRE Metadata Regulation INS MD, Part D6. The Responsible Party Role shall be mapped to the wms:ContactPosition of the wms:ContactInformation element

**Prerequisites**

* [Schema validation](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/schema-validation)

**Test method**

* This test only applies to [Scenario 2](#scenario-2). Otherwise the test case is skipped.
* Check if there is a [ContactPosition](#ContactPosition) node in the [ContactInformation](#ContactInformation) section
* If yes, check if that it has one of the values: resourceProvider, custodian, owner, user, distributor, originator, pointOfContact, principalInvestigator, processor, publisher, author.

**Reference(s)**:

* [TG VS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/README#ref_TG_VS), Chapter 4.2.3.3.1.14, Requirement 26


**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/README#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
ContactPosition <a name="ContactPosition"></a> | ./wms:Service/wms:ContactInformation/wms:ContactPosition
ContactInformation <a name="ContactInformation"></a> | ./wms:Service/wms:ContactInformation/wms:ContactPositionequals/text() equals ('resourceProvider' or 'custodian' or 'owner' or 'user' or 'distributor' or 'originator' or 'pointOfContact' or 'principalInvestigator' or 'processor' or 'publisher' or 'author')
Scenario 2 <a name="scenario-2"/> | ./wms:Capability/inspire_vs:ExtendedCapabilities[inspire_common:ResourceLocator or inspire_common:ResourceType or inspire_common:TemporalReference or inspire_common:Conformity or inspire_common:MetadataPointOfContact or inspire_common:MetadataDate or inspire_common:SpatialDataServiceType or inspire_common:MandatoryKeyword or inspire_common:Keyword]
