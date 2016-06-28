# Date type

**Purpose**: To be compliant with the INSPIRE Metadata Regulation INS MD and with ISO 19115 one of following dates shall be used: date of publication, date of last revision, or the date of creation. Date of last revision is preferred. The date shall be expressed in conformity with the INS MD.

**Prerequisites**

* Test for the existence of default element namespace.
* Test for the existence of the namespaces for INSPIRE View Services inspire_vs and inspire_common.

**Test method**

* Check if there is either a DateOfCreation node, a DateOfPublication node or a DateOfLastRevision node in the TemporalReference section.


**Reference(s)**:
* [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.3.1.9

**Test type:** Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
DateOfCreation <a name="DateOfCreation"></a> | /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:TemporalReference/inspire_common:DateOfCreation
DateOfPublication <a name="DateOfPublication"></a> | /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:TemporalReference/inspire_common:DateOfPublication
DateOfLastRevision <a name="DateOfLastRevision"></a> | /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:TemporalReference/inspire_common:DateOfLastRevision
TemporalReference <a name="TemporalReference"></a> | /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:TemporalReference
