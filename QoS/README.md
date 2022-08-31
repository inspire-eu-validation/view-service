# Conformance class: INSPIRE Quality of Service

This conformance class is part of the [Abstract Test Suite for the INSPIRE View Services Technical Guidance](http://inspire.ec.europa.eu/id/ats/view-service/3.2.0).

## Standardization target type

OGC web service WMS 1.3.0

OGC web service WMTS 1.0.0

## Dependencies

### Direct dependencies

A direct dependency is another conformance class whose requirements must be met by the view service, too.

| Specification | Conformance class | Parameters | 
| ------------- | ----------------- | ---------- |
| [Technical Guidance for the implementation of INSPIRE View Services 3.2.0](#ref_TG_VS) | [INSPIRE Profile of ISO 19128 / WMS 1.3.0](http://inspire.ec.europa.eu/id/ats/view-service/3.11/iso-19128) | n/a |

### Indirect dependencies

n/a
 
## External document references

| Abbreviation | Document name                       |
| ------------ | ----------------------------------- |
| INSPIRE <a name="ref_INSPIRE"></a> | [Directive 2007/2/EC of the European Parliament and of the Council of 14 March 2007 establishing an Infrastructure for Spatial Information in the European Community (INSPIRE)](http://eur-lex.europa.eu/legal-content/EN/TXT/PDF/?uri=CELEX:32007L0002&from=EN)
| TG VS <a name="ref_TG_VS"></a>   | [Technical Guidance for the implementation of INSPIRE View Services 3.2.0](https://inspire.ec.europa.eu/documents/technical-guidance-implementation-inspire-view-services-1)

## TG Requirement coverage

Based on requirement of the compliance with the Quality of Service as defined in Annex I of the NS regulation:

| Req#   | Description                          | Covered by test(s)                 | IR reference(s)                  |
| ------ | ------------------------------------ | ---------------------------------- | -------------------------------- |
| 1      | Performance: For a 470 Kilobytes image (e.g. 800x600 pixels with a colour depth of 8 bits), the response time for sending the initial response to a Get Map Request to a view service shall be maximum 5 seconds in normal situation     | n/a                                | n/a                              |
| 2      | Capacity: The minimum number of served simultaneous service requests to a view service according to the performance quality of service shall be 20 per second.    | n/a                                | n/a                              |
| 3      | Availability: The probability of a Network Service to be available shall be 99% of the time.     | n/a                                | n/a                              |

