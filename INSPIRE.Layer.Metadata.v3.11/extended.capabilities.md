# extended.capabilities

**Purpose**: The metadata response parameters shall be provided through the service Capabilities. These capabilities are mandatory and defined when a WMS or WMTS is set up. They consist of service information, supported operations and parameters values. INSPIRE requires additional metadata (extended capabilities).

**Prerequisites**

* [schema.valid](schema.valid.md)

**Test method**

* Check that the [ExtendedCapabilities](#extendedCapabilities) exist.

**Reference (s)**: 

* [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.3.1, Requirement 6
* [TG VS](README.md#ref_TG_VS), Chapter 5.2.3.3.1

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                     |  XPath expression												|  Parameter  value
------------------------------------------------ | ---------------------------------------------------------------	| ---------------------------------------------------------------
ExtendedCapabilities <a name="extendedCapabilities"></a>   | /wms:WMS_Capabilities/wms:Capability/inspire_vs:ExtendedCapabilities | ISO 19128
                                                           | /wmts:Capabilities/ows:OperationsMetadata/inspire_vs_ows11:ExtendedCapabilities | ISO 19128
