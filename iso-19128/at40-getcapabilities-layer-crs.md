# Layer coordinate Reference system

**Purpose**: Test that a supported CRS is provided based on ETRS89 for continental Europe and on ITRS outside continental Europe.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

  * For each wms:Layer element:

    * Check that at least one supported coordinates reference system is provided as a [CRS](#crs) element.

    * Check that CRS value is either a URL identifier or a label with namespace "EPSG", "CRS" or "AUTO2".

**Reference(s)**
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.4.7, Requirement 40

**Test type**: Automated

**Notes**

The multiplicity of this element is 1 or more.

A geographical coordinate system based on ETRS89 must be used in continental Europe and ITRS outside continental Europe.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
CRS <a name="crs"></a> | wms:Capability/wms:Layer/wms:CRS
