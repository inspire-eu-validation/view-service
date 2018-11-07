# Point of Contact

**Purpose**: Test that are provided a OrganisationName and Emailaddress elements within the MetadataPointOfcontact section.

**Prerequisites**

**Test method**

This test only applies to [scenario 2](./README.md#scenarios). Otherwise the test case is skipped.

* Send a getCapabilities request to the service endpoint. Into the response:

  * Check if is provided an [OrganisationName](#OrganisationName) node and a [EmailAddress](#EmailAddress) node in the MetadataPointOfContact section.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.1.15, Requirement 27

**Test type**: Automated

**Notes**

The multiplicity of this element is 1 or more.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
OrganisationName <a name="OrganisationName"></a> | wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:MetadataPointOfContact/inspire_common:OrganisationName
EmailAddress <a name="EmailAddress"></a> | wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:MetadataPointOfContact/inspire_common:EmailAddress