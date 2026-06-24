# Source Basis

Use this file when a user asks why a rule exists, wants primary-source justification, or needs to
audit the skill against real policy sources.

## Source map

| Skill rule | Primary support |
|---|---|
| Original research needs a Data Availability statement. | Most peer-reviewed journals now require a data availability statement for original research articles (ACM, IEEE, USENIX, Springer Nature, etc.). |
| The statement must cover original and reused data, including data that cannot be public. | Standard data policies apply to datasets needed to interpret and replicate conclusions and explicitly include original/reused data and non-publicly shareable data. |
| Supporting data should be public where possible, with mandatory community repositories for some data types. | Common policy strongly encourages public availability for datasets supporting analysis and conclusions and mandates sharing for community-endorsed data types. |
| Reviewers may need access to underlying data and code. | Many venues state peer reviewers are entitled to request access to underlying data and code when needed for evaluation. |
| Publication-ready statements must expose the minimum dataset needed to interpret, verify, and extend the work. | Venue reporting standards describe transparent access conditions for the minimum dataset needed to interpret, verify, and extend research. |
| Materials, data, code, and protocols should be available without undue qualifications, and restrictions must be disclosed. | Standard reporting policies state availability is a publication condition and restrictions must be disclosed at submission and in the manuscript. |
| Repositories are preferred over large supplementary files. | Modern data policies discourage large datasets in supplementary information and prefer repositories. |
| Repository choice should prefer discipline-specific, community-recognised repositories, with generalist or institutional repositories as fallback. | Repository guidance from multiple venues recommends discipline-specific community repositories where possible, otherwise generalist or institutional repositories. |
| Sensitive data should use safe sharing, controlled access, metadata records, or trusted environments where appropriate. | Sensitive data guidance recommends repository use where possible, controlled-access repositories, trusted research environments, and metadata records for non-public data. |
| Human, non-human sensitive, proprietary, and third-party data need explicit rights and access logic. | Sensitive data guidance from multiple sources lists identifiable human data, other sensitive data, and proprietary/third-party data as categories requiring special handling. |
| Rawness and reusability should follow community norms. | Community norms dictate data should be provided at a level of rawness allowing reuse in line with accepted community standards. |
| FAIR checks should include findability, accessibility, interoperability, and reusability for humans and machines. | Wilkinson et al. formally describe the FAIR principles and emphasize findable, accessible, interoperable, reusable digital objects for people and machines. |
| Dataset citation metadata should include persistent identifiers and core descriptive fields. | DataCite Metadata Schema defines core metadata properties for accurate and consistent identification, citation, and retrieval of resources. |

## Official sources

- ACM Artifact Review and Badging:
  <https://www.acm.org/publications/policies/artifact-review-and-badging-current>
- IEEE PSPB Operations Manual (Data Availability section):
  <https://pspb.ieee.org/images/files/files/opsmanual.pdf>
- USENIX Open Access Policy:
  <https://www.usenix.org/conferences/open-access-policy>
- Springer Nature, Research data policy:
  <https://www.springernature.com/gp/journal-policies/15369670>
- Springer Nature, Data availability statements:
  <https://www.springernature.com/gp/authors/research-data-policy/data-availability-statements>
- Springer Nature, Data repository guidance:
  <https://www.springernature.com/gp/authors/research-data-policy/recommended-repositories>
- Springer Nature, Sensitive data:
  <https://www.springernature.com/gp/authors/research-data-policy/sensitive-data>
- Nature Portfolio, Reporting standards and availability of data, materials, code and protocols:
  <https://www.nature.com/nature-portfolio/editorial-policies/reporting-standards>
- Wilkinson et al. 2016, The FAIR Guiding Principles for scientific data management and stewardship:
  <https://www.nature.com/articles/sdata201618>
- DataCite Metadata Schema:
  <https://schema.datacite.org/>

## Venue-specific guidance

- For ACM conferences (e.g., CCS, S&P), check the ACM Artifact Review and Badging policy.
- For IEEE venues, check the IEEE PSPB operations manual for data availability guidelines.
- For USENIX venues, the open access policy governs data and code sharing expectations.
- For Springer Nature journals, use the research data policy links above.
- Always check your specific target venue's author guidelines first, as policies can vary.

## Notes for future updates

- Check target venue instructions first because different venues can add field-specific requirements.
- Check DataCite's latest schema before naming version-specific fields. As of 2026-05-01, the
  DataCite schema landing page lists Metadata Schema 4.7 as the latest release.
- Keep this file as a source map, not a long policy mirror. Link to official pages rather than
  copying full policy text.
