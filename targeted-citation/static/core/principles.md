# Core principles (citation)

Use this skill to turn manuscript text into a defensible citation export:

- segmented text with citation candidates for each segment
- a reference-manager import file in `.enw`, `.ris`, or Zotero `.rdf`
- conservative evidence notes explaining whether each candidate truly supports the segment

## Default scope

Interpret venue scope from the user's wording, but keep the filter strict:

- `security-top4`: search IEEE S&P, ACM CCS, NDSS, USENIX Security first. These are the four most prestigious cybersecurity conferences.
- `security-all`: search top4 plus ACSAC, RAID, ESORICS, PETS, CSF, AsiaCCS, and other recognized security venues.
- `cs-conferences`: broader CS including top AI/ML venues that publish security-related work (AAAI, IJCAI, NeurIPS, ICML, ICLR), plus all security venues.
- `custom`: the user provides a specific venue list or CORE/CCF tier.

Do not treat merely related journals or conferences as in-scope. A venue is valid only if it is in the accepted CS/security venue list or clearly matches the user's custom specification. If the user needs an exhaustive or submission-critical boundary, verify current CORE rankings or CCF recommended lists before finalizing. The exact boundary and official source notes are in `references/journal-scope.md`.

## Source hierarchy

Use sources in this order:

1. Structured bibliographic metadata: DBLP, Crossref, IEEE Xplore, ACM Digital Library, DOI metadata.
2. Publisher/conference pages: `ieee-security.org`, `acm.org`, `usenix.org`, `ndss-symposium.org`, and official proceedings pages.
3. Full text or abstract pages, if accessible.
4. Secondary databases such as Google Scholar, Semantic Scholar, Web of Science, or Scopus only as discovery aids, not as the sole support basis.

Prefer structured APIs for metadata and publisher/proceedings pages for claim verification. If metadata and proceedings page disagree, preserve the DOI and venue facts and flag the discrepancy.

## Search quality rules

- Prefer precision over volume. A useful answer is usually 3-8 candidates, not 50 loosely related papers.
- Use exact phrase searches only for distinctive terms; otherwise use concept terms and synonyms.
- Check venue identity. Many venues have similar names; verify the official proceedings or publisher page.
- Treat citation count as a tie-breaker, not evidence of support.
- Capture retractions, corrections, and expressions of concern when visible in Crossref or publisher metadata.
- Date-sensitive topics require current searching and an explicit search date.
- For medical, clinical, or safety claims, search current literature and state that citations do not replace clinical guidance or systematic review.

## Source notes

This skill is based on public bibliographic APIs and official publisher/import documentation: Crossref REST API and filters, DBLP, IEEE Xplore, ACM Digital Library, EndNote RIS import options, CS conference proceedings and journal descriptions, and CORE/CCF venue rankings. Verify pages at use time when exact venue coverage or current import behavior matters.
