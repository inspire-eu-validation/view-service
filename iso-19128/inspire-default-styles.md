# Inspire default styles

**Purpose**: To make combining of layers from different INSPIRE data providers possible, the layers portraying harmonized particular INSPIRE datasets must be made available with the same harmonized INSPIRE rendering styles
as specified in the Data Specification documents for each theme.

**Prerequisites**

* [Schema validation](./schema-validation.md)
* [Harmonised layer name](./harmonised-layer-name.md)

**Test method**

For each [Layer](#layer) qualified as presenting an inspire harmonized dataset during the previously run 
test [harmonised layer name](./harmonised-layer-name.md):
* For each [Style element](#style) within the Layer:
  * If no required default style for this layer is given in the INSPIRE Data Specification in which this harmonized layer name is introduced, pass the test for this layer. Otherwise:
    * Check if the [Style Name](#style-name) equals the name of the default style name for this layer as defined by the Portrayal section of the INSPIRE Data Specification of the INSPIRE theme.
* If none of the [Style Name](#style-name) elements match, repeat the test recursively for any parent Layer until a match is found or there is no parent layer (1). If no match was found in the end, fail the test for the original layer.
* All layers not qualified as presenting INSPIRE harmonized datasets must be ignored in running this test.

**Reference(s)**:

* [TG VS](./README.md#ref_TG_VS), chapter 4.2.3.3.4.8, Requirement 42

**Test type**: Automated

**Notes**

1. Note that the parent layers do not have to be qualified as INSPIRE harmonized layers to be included in the recursive style name matching.

## Contextual XPath references

The namespace prefixes used as described in [README.md](./README.md#namespaces).

Abbreviation                                               |  XPath expression (relative to wms:WMS_Capabilities)
---------------------------------------------------------- | -------------------------------------------------------------------------
Layer <a name="layer"></a> | ./wms:Capability/\./wms:Layer
Style <a name="style"></a> | ./wms:Capability/\./wms:Layer/wms:Style
Style Name <a name="style-name"></a> | ./wms:Capability/\./wms:Layerwms:Style/wms:Name

