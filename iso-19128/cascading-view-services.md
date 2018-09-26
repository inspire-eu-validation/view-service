# Review cascading view services

**Purpose**: If the Member State's View Service supports cascading and is responsible for collating the maps from third party View Service providers, the configuration needs to be checked.

**Prerequisites**

**Test method**

This test case only applies for view services that support cascading of other view services.

Check that
* the cascading View Service includes the cascaded services' layer metadata in his own service metadata,
* the 'cascaded' attribute of the wms:Layer element is used to indicate that the layer is hosted by a remote View Service and the level of the cascade,
* the cascading View Service sends requests to the cascaded View Services with the transparency parameter (TRANSPARENT) of the WMS GetMap request set to 'true' 
and the background parameter (BGCOLOR) for all layers  set to the same colour.
    
**Reference(s)**: 

* [TG VS](./README#ref_TG_VS), Chapter 4.2.5.3, Requirements 62, 63, 64

**Test type**: Manual

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
