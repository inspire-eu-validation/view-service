# Contact person

**Purpose**: Responsible Party as described in the INSPIRE Metadata Regulation INS MD shall be mapped to the wms:ContactOrganization element of the wms:ContactPersonPrimary within the wms:ContactInformation element.

**Prerequisites**

* [Schema validation](./schema-validation.md)

**Test method**

* Check if there is a [ContactOrganization](#ContactOrganization) node in the [ContactPersonPrimary](#ContactPersonPrimary) element of the [ContactInformation](#ContactInformation) section.

**Reference(s)**:

* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.1.14, Requirement 25


**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
ContactInformation <a name="ContactInformation"></a> | ./wms:Service/wms:ContactInformation
ContactPersonPrimary <a name="ContactPersonPrimary"></a> | ./wms:Service/wms:ContactInformation/wms:ContactPersonPrimary
ContactOrganization <a name="ContactOrganization"></a> | ./wms:Service/wms:ContactInformation/wms:ContactPersonPrimary/wms:ContactOrganization
