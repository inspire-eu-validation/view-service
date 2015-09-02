# A.38.IR45.IR47.style.legend.url

**Purpose**: Legend is required for explaining the data visualization used for each layer. If the legend contains
language-specific elements, localized legends shall be made available in each localized capabilities document.

**Prerequisites**

* [A.03.IR05.schema.validation](A.03.IR05.schema.validation.md)
* [A.34.IR46.style.node](A.34.IR46.style.node.md)
* [A.35.IR39.harmonized.layer.name](A.35.IR39.harmonized.layer.name.md)

**Test method**

For each [Layer](#Layer) qualified as presenting an INSPIRE harmonized dataset during the previously run test [A.35.IR39.harmonized.layer.name](A.35.IR39.harmonized.layer.name.md):
* Check that for each [Style element](#style):
  * There exists a non-empty [href attribute](#href) in the OnlineResource element. Let the value of the attibute be ```href```.
  * Resolve and download the Internet resource referred to by ```href```. If the download is successful and a non-empty image file returned:
    * If the [Format element](#format) equals 'image/gif' or 'image/png':
      * the downloaded resource must be a valid image of these image formats correspondingly. If it is, pass the test. If not, fail the test for this Style.
    * Otherwise, pass the test for this Style.
  * Otherwise, fail the test for this Style

**Reference(s)**

* [TG VS](README.md#ref_TG_VS), chapter 4.2.3.3.4.8 Styles
* [IR NS](README.md#ref_IR_NS), Annex III, Part A, 2.2.4. Layers Metadata parameters

**Test type**: Automated

**Notes**

* Interpreted as to be applicable only to layers with an INSPIRE harmonized name.
* Note that it's generally not required for the validator to recognize the image formats of the downloaded legend files in order to pass the test.

## Contextual XPath references

The namespace prefixes used as described in [README.md](README.md#namespaces).

Abbreviation                                               |  XPath expression
---------------------------------------------------------- | -------------------------------------------------------------------------
Layer <a name="layer"></a> | /wms:WMS_Capabilities/wms:Capability//wms:Layer
Style element <a name="style"></a> | ./wms:Style
href attribute <a name="href"></a> | ./wms:Style/wms:LegendURL/wms:OnlineResource/@xlink:href
Format element <a name="format"></a> | ./wms:Style/wms:LegendURL/wms:Format
