# Contact position

**Purpose**: The value domain of the Responsible Party role shall comply with the INSPIRE Metadata Regulation INS MD, Part D6. The Responsible Party Role shall be mapped to the wms:ContactPosition of the wms:ContactInformation element

**Prerequisites**

* [Schema validation](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/schema-validation)

**Test method**

* Check if there is a ContactPosition node in the ContactInformation section
* If yes, check if that it has one of the values: resourceProvider, custodian, owner, user, distributor, originator, pointOfContact, principalInvestigator, processor, publisher, author.

**Reference(s)**:

* [TG VS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/README#ref_TG_VS), Chapter 4.2.3.3.1.14

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
ContactPosition <a name="ContactPosition"></a> | /wms:WMS_Capabilities/wms:Service/wms:ContactInformation/wms:ContactPosition
ContactInformation <a name="ContactInformation"></a> | /wms:WMS_Capabilities/wms:Service/wms:ContactInformation
