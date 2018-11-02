# Mapping of service metadata elements

**Purpose**: Test that 

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * Check if a [Title](#title) element is provided and is not empty.

  * Check if an [Abstract](#abstract) element is provided and is not empty.

  * Check if at least one [AccessConstraints](accessConstraints) element is provided

**Reference(s)**
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.1, Requirement 10

**Test type**: Automated

**Notes**

The multiplicity of Title and Abstract elements is 1.

The multiplicity of AccessConstraints element is 1 or more.

As stated by the INSPIRE Metadata Technical Guidance [INS MDTG], it is not possible to express the restriction of a service concerning the spatial resolution in the current version of [ISO 19119].
While this issue is being addressed by the standardisation community, spatial resolution restrictions for services shall be written in the Abstract as mandated by the Metadata Technical Guidance [INS MDTG]. Spatial Resolution restrictions at service metadata
level shall be declaratively described in the wms:Abstract element.

For the AccessConstraints element, is recomended to use "None" value when any constrainst is applied and when constraints are imposed may be used the codelists defined in [ISO 19115, Annex B – Data Dictionary, Section 5.24].

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Title <a name="title"></a> | wms:Service/wms:Title
Abstract <a name="abstract"></a> | wms:Service/wms:Abstract
Access Constraints <a name="accessConstraints"></a> | wms:Service/wms:AccessConstraints
