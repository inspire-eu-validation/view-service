# Check Title and Abstract

**Purpose**: A View Service must contain a non-empty Title and Abstract to fulfill the INSPIRE Metadata requirements for Resource Title, Resource Abstract and Spatial Resolution.

**Prerequisites**

* Test for the existence of default element namespace.

**Test method**

* Check that both [Title](#title) and [Abstract](#abstract) exist and are non-empty. If so, pass the test. Otherwise fail the test.


**Reference(s)**:
* [TG VS](README.md#ref_TG_VS), Requirement 10, Chapter 4.2.3.3.1

**Test type:** Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
Title <a name="title"></a> | /wms:WMS_Capabilities/wms:Service/wms:Title
Abstract <a name="abstract"></a> | /wms:WMS_Capabilities/wms:Service/wms:Abstract
