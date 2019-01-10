# Contact Position

**Purpose**: Test that the responsible party role is mapped to the ContactPosition element within the ContactInformation section.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * Check if there is a [ContactPosition](#ContactPosition) node within the [ContactInformation](#ContactInformation) section. If it does,

    * Check if it has one of the following values: resourceProvider, custodian, owner, user, distributor, originator, pointOfContact, principalInvestigator, processor, publisher, author.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.1.14, Requirement 26

**Test type**: Automated

**Notes**

The multiplicity of this element is 1 or more.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
ContactInformation <a name="ContactInformation"></a> | wms:Service/wms:ContactInformation
ContactPosition <a name="ContactPosition"></a> | wms:Service/wms:ContactInformation/wms:ContactPosition