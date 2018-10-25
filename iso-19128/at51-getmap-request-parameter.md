# GetMap Request Parameter

**Purpose**

Test that the REQUEST paramater in GetMap operation is mandatory.

**Prerequisites**

**Test method**

* Send a request without REQUEST parameter and all the other mandatory parameters.
    * Check that the service notify the missing parameter.
* Send a request with an invalid REQUEST parameter and all the other mandatory parameters.
    * Check that the service notify the invalid parameter value.
* Send a request with 'GetMap' value for REQUEST parameter and all the other mandatory parameters.
    * Check that the service response is a correct document.

**Reference(s)**:

* [TG VS](./README.md#ref_TG_VS), requirement 51

**Test type**: Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
