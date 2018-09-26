# Extended Capabilities

**Purpose**: The metadata response parameters shall be provided through the service Capabilities.
These capabilities are mandatory and defined when a WMS is set up. They consist of service information, supported operations and parameters values. INSPIRE requires additional metadata (extended capabilities).

**Prerequisites**

* [Schema validation](./schema-validation.md)

**Test method**

* Check that the [ExtendedCapabilities](#extendedCapabilities) exist. If yes:
  * Validate the [ExtendedCapabilities](#ExtendedCapabilities) element and it's children according to the XML Schema definition for the INSPIRE Extended Capabilities as defined in the http://inspire.ec.europa.eu/schemas/inspire_vs/1.0/inspire_vs.xsd

* If no ExtendedCapabilities were found or validation fails, fail the test.

**Reference (s)**: 

* [TG VS](./README.md#ref_TG_VS), Chapter 4.3.1, Requirement 72

**Test type**: Automated

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
ExtendedCapabilities <a name="extendedCapabilities"></a>   | ./wms:Capability/inspire_vs:ExtendedCapabilities
