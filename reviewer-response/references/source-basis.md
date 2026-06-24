# Source basis

Use this file to keep `reviewer-response` grounded in general best-practice academic peer-review
process sources. Source labels distinguish formal policy from journal instructions and editorial
advice.

## Source hierarchy

1. Target journal or conference instructions and the specific editor decision letter.
2. The venue's own peer-review and revision guidelines.
3. General editorial advice on reviewer response letters.
4. Local manuscript facts supplied by the author.

If a current journal page conflicts with this file, follow the current journal page.

## Sources and rules

No single URL set covers all academic venues. Apply these general principles drawn from
established best-practice guidance:

| Principle | Source type | Local rule summary |
|---|---|---|
| Point-by-point response structure | General editorial best practice | Revised papers that need technical work should be accompanied by a point-by-point response to reviewer comments. Resubmitted manuscripts must seriously address reviewer criticisms unless the editor says otherwise. |
| Transparent review artifacts | General editorial best practice | Reviewer comments and author rebuttal material may be published alongside accepted manuscripts in some venues. Write response letters as potentially auditable public documents. |
| Revision package contents | General editorial best practice | A revision package commonly includes the revised manuscript, a response to each reviewer, and (for many journals) a cover letter. This skill handles the reviewer response; cover-letter generation is out of MVP scope. |
| Rebuttal letter writing guidance | General editorial advice | Preserve reviewer comments, respond immediately after each concern, number or clearly separate replies, state where changes appear, and avoid venting, accusations, ignored requests, or distorted paraphrases. |
| Appeal vs. revision routing | General editorial best practice | Appeals and revision responses follow different logic, so appeal-like cases should be routed separately instead of treated as ordinary point-by-point revision responses. |

**Note for CS/security conferences (ACM CCS, IEEE S&P, NDSS, USENIX Security):** Response letters are typically less formal than Nature-family journals, often do not require separate cover letters, and reviewers may expect responses grouped by reviewer number.

## Implementation implications

- Point-by-point response is the default structure for revision cases.
- Every referee criticism must be answered, justified, cross-referenced, or flagged as unresolved.
- A cover letter can be mentioned as adjacent revision-package material, but this skill does not draft it by default.
- The skill should copy or preserve reviewer wording supplied by the user unless the user asks for anonymization or summarization.
- Tone, accuracy, and traceability should meet the standard of material that may later be reviewed by editors, reviewers, or public readers.
