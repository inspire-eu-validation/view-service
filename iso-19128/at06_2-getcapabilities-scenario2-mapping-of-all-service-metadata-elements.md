# Scenario 2 - Mapping of service metadata elements

**Purpose**: Test that the capabilities section of the View Service contains the Service metadata elements in accordance with Table 3a (Mapping between INSPIRE metadata elements and [ISO 19128] WMS elements with the use of extended capabilities).

**Prerequisites**

This test only applies to [Scenario 2](./README.md#scenarios). Otherwise the test case is skipped.

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response, check that all the service metadata elements are provided and they are not empty, according to the table below:



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

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------

