# 31. Changing 5 attributes from Mandatory to Optional

Date: 2024-03-13

## Status

Proposed

## Context

Feedback was raised by the PACT Community that some mandatory fields should be reconsidered whether they should be mandatory. The five fields below were ultimately determined to be in-scope for this decision. Other mandatory attributes to be considered to be made optional can be considered in a separate ADR.

* ```productDescription```
* ```boundaryProcessDescription```
* ```comment```
* ```exemptedEmissionsDescription​```
* ```productCategoryCpc```

A brief rationale for the following proposal is summarized below. Detailed rationale can be found in the PACT Decision Log, linked below for each attribute.

| Attribute    | Summarized Rationale  |
| -------- | ------- |
|  [productDescription](https://flat-dollar-c04.notion.site/productDescription-Mandatory-OR-Optional-2a2d574150904800a1f454ffc9f3d7b9?pvs=74) | Free-form text field which is not populated in a standardized way and labor intensive to generate at scale.      |
| [boundaryProcessDescription](https://flat-dollar-c04.notion.site/boundaryprocessdescription-Mandatory-OR-optional-882d5bd259c143758f01dd53656d32b4) | Free-form text field which is not populated in a standardized way and labor intensive to generate at scale. Best to be standardized in a data model extension.     |
| [comment](https://flat-dollar-c04.notion.site/Comment-Mandatory-OR-Optional-a40cc26d5bfb4095be125b883da263ef)    | Free-form text field which is not populated in a standardized way and labor intensive to generate at scale.   |
| [exemptedEmissionsDescription](https://flat-dollar-c04.notion.site/exemptedEmissionsDescription-Mandatory-OR-Optional-35903b06402e4e5dbeb02ef2a77bba2f?pvs=74)    | Free-form text field which is not populated in a standardized way and labor intensive to generate at scale.    |
| [productCategoryCpc](https://flat-dollar-c04.notion.site/productCategoryCPC-Mandatory-OR-Optional-c6963fc3aa31451ba10ef05e159de513)    | UN Product Classification Code (CPC) classification system was not recognized to be used by most companies and therefore brought undue burden if required to be populated.   |

## Decision

* The topic was presented to both Technology and Methodology WGs
* It was decided to create a sub-working-group to form consensus, jointly between Technology and Methodology WGs
* Initiatives (TfS, Catena-X, and Green x Digital) endorse changing all 5 attributes to optional
* The sub-working-group met March 7, 2024 and formed consensus all 5 attributes should become optional
* The Technology WG met March 13 and formed consensus approving all 5 attributes to become optional, adopting the proposal from the sub-working-group
* The Methodolgy WG met March 28 and formed consensus approving 4 of the 5 attributes to become optional; objections were raised that ```productDescription``` should not become optional as this field is still necessary to be used to uniquely identify products and by making this optional it will become even more challenging to uniquely identify the product to which the PCF refers. The objection is now being raised in writing from the members and a final decision will be reached in Q2. Meanwhile, advisements have been added to the v2.2 Tech Specs release for the 4 attributes which have reached consensus to become optional.

## Consequences

Changing attributes from Mandatory to Optional results in a backwards-breaking change. Thus this proposal will be reflected in v3 of the Tech Specs. However, in a minor version (v2.x.x) an advisement should be included to indicate these attributes will become optional in v3.
