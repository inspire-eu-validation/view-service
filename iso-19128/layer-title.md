# Layer title

**Purpose**: Layer title is mapped with the corresponding Title element in the Capabilities. The harmonised title of a layer for an INSPIRE spatial data theme is defined by INS DS and shall be subject to multilingualism (translations shall appear in each mono-lingual capabilities localised documents).

**Prerequisites**

* [Schema validation](./schema-validation)

**Test method**

For each Layer element provided check that the [Title element](#Title) is a non-empty character string.

**Reference(s)**:

* [TG VS](./README#ref_TG_VS), Chapter 4.2.3.3.4.1, Requirement 33

**Test type**

Automated

**Notes**

The validation of the correctness of the translated title is not done due to it's complexity and the controversy over the usefulness of the harmonised layer titles. If this is decided to be necessary, the procedure should be similar to one used in `A.04.layer.name.id`.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Title <a name="Title"></a> | ./wms:Capability/wms:Layer/wms:Title

