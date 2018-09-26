# Dimension

**Purpose**: A WMS server can provide support for several type of dimensions such as time, elevation or other types of dimensions (for example, satellite images in different wavelength bands).

**Prerequisites**

* [Schema validation](./schema-validation)

**Test method**

* Check if the map is fully defined by its two-dimensional axis in the [CRS](#CRS). 
* In other cases a map can defines by other params of dimensions, for example time and elevation, [Dimension](#dimension) and must be used the wms:Dimension element according to [INS NS]:

* @name --> The [name](#name) of the field in the DB that contains the dimension values.
* @units --> [Units](#units) of dimensional axis. 
  * If the dimensional quantity has no units use the null string.
  * If yes, unit names should be taken from the Unified Code for Units of Measure (UCUM) if UCUM has an appropriate entry. When UCUM is used, the mandatory units attribute shall be an appropriate entry from the UCUM “name” column

**Reference(s)**:
* [TG VS](./README#ref_TG_VS), Chapter 4.2.3.3.4.10, Requirement 48

**Test type**: Automated

**Notes**

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
CRS <a name="CRS"></a> | ./wms:Service/\./Layer/wms:CRS
Dimension <a name="dimension"></a> | ./wms:Service/\./Layer/wms:Dimension
Name <a name="name"></a> | ./wms:Service/\./Layer/wms:Dimension[1]/@name
Units <a name="units"></a> | ./wms:Service/\./Layer/wms:Dimension[1]/@units
