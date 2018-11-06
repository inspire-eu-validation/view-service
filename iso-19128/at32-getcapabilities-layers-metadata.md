# View Service Metadata in Discovery Service

**Purpose**: Test that the layer description shall use elements defined for the service capabilities in the [ISO 19128] standard.

**Prerequisites**

**Test method**

**Reference(s)**
* [TG VS](./README.md#ref_TG_VS), Chapter 4.2.3.3.4, Requirement 32

**Test type**: None

**Notes**

The mapping between INSPIRE layer metadata elements and ISO 19128 WMS elements is implemented in the Abstract Tests from [at33](./at33-getcapabilities-layer-title.md) to [at48](./at48-getcapabilities-layer-dimension-pairs.md).

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Example <a name="example"></a> | ./wms:Service/wms:Example
