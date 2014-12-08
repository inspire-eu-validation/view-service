# Raw notes from the MD & NS validation workshop

General notes: There should be a clear separation of the requirements for scenario 1 (INSPIRE metadata provided using
the remote metadata record) and scenario 2 (metadata provided inline within the INSPIRE ExtendedCapabilities).

It was decided that the ATS for WMS will reflect this separation by arranging the metadata validity tests
in two high-level tests for each scenario. Each of these tests contain the necessary sub-level tests
required for validating a service for that scenario.

The validation flow path is selected by checking the existence if the inline-scenario elements: If at least one
of any of the following elements are found within the ExtendedCapabilities, the validator must validate
the service using the scenario 2:

* ResourceLocator,
* ResourceType,
* TemporalReference,
* Conformity,
* MetadataPointOfContact,
* MetadataDate,
* SpatialDataServiceType,
* MandatoryKeyword,
* Keyword

If none of these elements are found in the ExtendedCapabilities, the validator must validate
the service using the scenario 1.

## Requirements 1,2 and 3

Combine Req 1, 2 & 3: Refer to WMS 1.3.0 ATS for A.1.2 "Basic WMS Server"

## Requirement 4

The capabilities doc must include exactly one INSPIRE ExtendedCapabilities element.
The INSPIRE ExtendedCapabilities element must be valid using the official
INSPIRE schema available at http://inspire.ec.europa.eu/schemas/inspire_vs/1.0

## Requirement 5

Covered by the Basic WMS Server CC

## Requirement 6

Branching point for validation scenarios 1 and 2.

In scenario 1:

* SupportedLanguages must exist (covered by schema validation),
* ResponseLanguage must exist (covered by schema validation),
* MetadataUrl must exist, and it's URL element must be a valid URL and it must resolve to a valid XML document with
   a valid gmd:MD_Metadata element as the root element. This MD_Metadata element must describe an INSPIRE View Service
   (according the the MD tests), and it's distributionInfo/\*/transferOptions/\*/onLine/\*/linkage must contain
   a URL reference to the WMS service Capabilities document under validation. This URL needs to be resolved in
   order to check that it return a capabilities document with the same MetadataURL as the original Capabilities document. Note that
   the URLs used for fetching the Capabilities documents, the contained OnlineResource addresses of the WMS operations or other
   contents of the capabilities documents do not have to match.

In scenario 2:

* SupportedLanguages must exist (covered by schema validation),
* ResponseLanguage must exist (covered by schema validation),
* All the mandatory INSPIRE metadata elements must exist and be valid (separate sub-tests for each element)

## Requirement 7

Covered by test for Requirement 6

## Requirement 8

Covered by schema validation

## Requirement 9

Should be a requirement for the metadata

## Requirement 12

For scenario 2 only: the same test as in the metadata ATS for this element

## Requirement 13

Note: not inherited from parent layers. At least one of the url resolves into a dataset or dataset series MD record.

## Requirement 14

Covered by tests for Requirement 13

## Requirement 15

Only for scenario 2

## Requirement 16

In scenario 1: the keyword must be contained in the fetched MD record.

In scenario 2: either the WMS or the extended capabilities Keywords must include one of these keywords.

## Requirement 17

Not really testable. Also no vocabulary date possible for the wms:KeywordList.
