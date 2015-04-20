# A.30.IR30.GetCapabilities.element.node

**Purpose**: EGetCapabilities operation metadata shall be mapped to the wms:GetCapabilities element.

**Prerequisites**

* Test for the existence of default element namespace.

**Test method**

* Then check if there is a GetCapabilities node in the Request section.

**Reference(s)**: 
* [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.3.2.1

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
GetCapabilities <a name="GetCapabilities"></a>   | WMS_Capabilities/Capability/Request/GetCapabilities
Request <a name="Request"></a>   | /WMS_Capabilities/Capability/Request
