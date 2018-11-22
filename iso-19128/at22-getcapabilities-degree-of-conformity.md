# Degree of conformity

**Purpose**: Test that is provided a Degree element indicating the degree of conformity with the implementing rules provided in Art. 7.1 (Interoperability of spatial data sets and services) of the INSPIRE Directive [Directive 2007/2/EC].

**Prerequisites**

**Test method**
This test only applies to [scenario 2](./README.md#scenarios). Otherwise the test case is skipped.

* Send a getCapabilities request to the service endpoint. Into the response:

  * Check that is given a [Degree](#Degree) node with one of these values: notEvaluated, conformant, notConformant.

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.1.11, Requirement 22
* [INSPIRE](./README.md#ref_INSPIRE), Art. 7.1 (Interoperability of spatial data sets and services)

**Test type**: Automated

**Notes**

The multiplicity of this element is 1.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Degree <a name="Degree"></a> | wms:Capability/inspire_vs:ExtendedCapabilities/inspire_common:Conformity/inspire_common:Degree