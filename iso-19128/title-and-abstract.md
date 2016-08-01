# Title and Abstract

**Purpose**: A View Service must contain a non-empty Title and Abstract to fulfill the INSPIRE Metadata requirements for Resource Title, Resource Abstract and Spatial Resolution.

**Prerequisites**

* [Schema validation](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/schema-validation)

**Test method**

* Check that both [Title](#title) and [Abstract](#abstract) exist and are non-empty. If so, pass the test. Otherwise fail the test.

**Reference(s)**:
* [TG VS](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/README#ref_TG_VS), Chapter 4.2.3.3.1, Requirement 10

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128/README#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
Title <a name="title"></a> | /wms:WMS_Capabilities/wms:Service/wms:Title
Abstract <a name="abstract"></a> | /wms:WMS_Capabilities/wms:Service/wms:Abstract
