# Response parameters through service Capabilities

**Purpose**: The metadata response parameters shall be provided through the service Capabilities, as defined in the WMS Standard ISO 19128, Section 7.2.4. These capabilities are mandatory and defined when a WMS is set up. They consist of service information, supported operations and parameters values.

**Prerequisites**

* Test for the existence of default element namespace.
* Test for the existence of the namespaces for INSPIRE View Services inspire_vs and inspire_common.
* [A.03.IR05.schema.validation](A.03.IR05.schema.validation.md) must be passed

**Test method**

* Check that the [ExtendedCapabilities](#ExtendedCapabilities) exists. If it does
  * Validate the [ExtendedCapabilities](#ExtendedCapabilities) element and it's children according to the XML Schema definition for the WMS INSPIRE extendedCapabilities as defined in the http://inspire.ec.europa.eu/schemas/inspire_vs/1.0/inspire_vs.xsd
  * If the validation passes, pass the test.
* If no ExtendedCapabilities were found or validation fails, fail the test.

**Reference (s)**: [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.1

**Test type:**  Automated

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
ExtendedCapabilities <a name="extendedCapabilities"></a>   | /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities
