# A.03.IR03.getcapabilities.getmap.node

**Purpose**: The following ISO 19128 operations shall be implemented for an INSPIRE View service: GetCapabilities, GetMap.

**Prerequisites**

* Test for the existence of default element namespace.

**Test method**

* Check if the service document contains the GetCapabilities and GetMap nodes in the request section.

**Reference (s)**: [TG VS](README.md#ref_TG_VS), Chapter 4.2

**Notes**


## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
GetCapabilities <a name="GetCapabilities"></a>   | /WMS_Capabilities/Capability/Request/GetCapabilities
GetMap <a name="GetMap"></a>   | /WMS_Capabilities/Capability/Request/GetMap
