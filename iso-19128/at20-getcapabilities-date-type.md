# Date type

**Purpose**: Test that one of the following dates (date of publication, date of last revision or date of creation) is provided.

**Prerequisites**

**Test method**

This test only applies to [scenario 2](./README.md#scenarios). Otherwise the test case is skipped.

* Send a getCapabilities request to the service endpoint. Into the response:

  * Check if it is provided at least one [DateOfPublication](#DateOfPublication), [DateOfLastRevision](#DateOfLastRevision) or [DateOfCreation](#DateOfCreation) element within inspire_vs:ExtendedCapabilities section.

  * Check if the provided date is formated in YYYY-MM-DD.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.1.9, Requirement 20

**Test type**: Automated

**Notes**

Is preferred to include the date of last revision.

The multiplicity of this element is 1 or more.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
DateOfPublication <a name="DateOfPublication"></a> | wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:TemporalReference/inspire_common:DateOfPublication
DateOfLastRevision <a name="DateOfLastRevision"></a> | wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:TemporalReference/inspire_common:DateOfLastRevision
DateOfCreation <a name="DateOfCreation"></a> | wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:TemporalReference/inspire_common:DateOfCreation