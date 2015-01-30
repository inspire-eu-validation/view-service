# A.26.IR26.contactposition.node

**Purpose**: The value domain of the Responsible Party role shall comply with the INSPIRE Metadata Regulation INS MD, Part D6. The Responsible Party Role shall be mapped to the wms:ContactPosition of the wms:ContactInformation element

**Prerequisites**

* Test for the existence of default element namespace.

**Test method**

* Check if there is a ConatctPosition node in the ContactInformation section
* If yes, check if that it has one of the values: resourceProvider, custodian, owner, user, distributor, originator, pointOfContact, principalInvestigator, processor, publisher, author.

**Reference(s)**: 
* [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.3.1.14

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
ContactPosition <a name="ContactPosition"></a> | /WMS_Capabilities/Service/ContactInformation/ContactPosition
ContactInformation <a name="ContactInformation"></a> | /WMS_Capabilities/Service/ContactInformation
