# A.31.IR31.getmap.format.node

**Purpose**: GetMap operation metadata shall be mapped to the wms:GetMap element. Either PNG or GIF format (without LZW compression) with transparency shall be supported by the View service INS NS, Annex III, Part B.

**Prerequisites**

* Test for the existence of default element namespace.

**Test method**

* Check if there is a GetMap node in the Request section 
* If yes, check if there is one Format node in the GetMap section with the value 'image/png' and and one with the value 'image/gif'.

**Reference(s)**: 
* [TG VS](README.md#ref_TG_VS), Chapter 4.2.3.3.2.2

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
GetMap <a name="GetMap"></a> | /WMS_Capabilities/Capability/Request/GetMap
Request <a name="Request"></a> | /WMS_Capabilities/Capability/Request
Format <a name="Format"></a> | /WMS_Capabilities/Capability/Request/GetMap/Format
