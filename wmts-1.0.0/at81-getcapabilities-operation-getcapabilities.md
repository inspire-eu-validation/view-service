# Operation GetCapabilities

**Purpose**: Test that an Operation element is provided to map the GetCapabilities operation.

**Prerequisites**

**Test method**

* Send a getCapabilities request to the service endpoint. Into the response:

    * Check that a [Operation](#operation) element is provided with a "name" attribute with a fix value equals to "GetCapabilities".

**Reference(s)**:
* [TG VS](./README.md#ref_TG_VS), Chapter 5.2.3.3.2.1, Requirement 81

**Test type**: Automated

**Notes**

The multiplicity of Operation element is 2 or more.

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Operation <a name="operation"></a> | ows:Operation