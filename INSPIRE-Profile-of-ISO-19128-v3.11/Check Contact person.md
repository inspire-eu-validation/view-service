# Check Contact person

**Purpose**: Responsible Party as described in the INSPIRE Metadata Regulation INS MD shall be mapped to the wms:ContactOrganization element of the wms:ContactPersonPrimary within the wms:ContactInformation element.

**Prerequisites**

* Test for the existence of default element namespace.
* Test for the existence of the namespaces for INSPIRE View Services inspire_vs and inspire_common.

**Test method**

* Check if there is a [ContactOrganization](#ContactOrganization) node in the [ContactPersonPrimary](#ContactPersonPrimary) element of the [ContactInformation](#ContactInformation) section.

**Reference(s)**:
* [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.3.1.14

**Test type:** Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
ContactInformation <a name="ContactInformation"></a> | /wms:WMS_Capabilities/wms:Service/wms:ContactInformation
ContactPersonPrimary <a name="ContactPersonPrimary"></a> | /wms:WMS_Capabilities/wms:Service/wms:ContactInformation/wms:ContactPersonPrimary
ContactOrganization <a name="ContactOrganization"></a> | /wms:WMS_Capabilities/wms:Service/wms:ContactInformation/wms:ContactPersonPrimary/wms:ContactOrganization
