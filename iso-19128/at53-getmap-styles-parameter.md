# GetMap Styles Parameter

**Purpose**

Test that the STYLES paramater in GetMap operation is mandatory.

**Prerequisites**

**Test method**

* Send a GetMap request without STYLES parameter and all the other mandatory parameters.

    * Check that the service notifies the missing parameter.

* Send a GetMap request with an invalid STYLES parameter and all the other mandatory parameters.

    * Check that the service notifies the invalid parameter value.

* Send a GetMap request with a valid value for STYLES parameter and all the other mandatory parameters.

    * Check that the service response is successful.

* Send a GetMap request with a list of valid INSPIRE styles separated by commas value for STYLES parameter and all the other mandatory parameters.

    * Check that the service response is successful.

* Send a GetMap request with a null value for STYLES parameter (STYLES=) and all the other mandatory parameters.

    * Check that the service response is successful.

**Reference(s)**:

* [TG VS](./README.md#ref_TG_VS), requirement 53

**Test type**: Automated

**Notes**

**Contextual XPath references**

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to /wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
