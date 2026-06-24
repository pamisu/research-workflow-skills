# Venue Scope (CS & Security)

The skill's default venue boundary targets top CS/security conferences and journals. Use it
to find likely top-venue candidates, then verify exact venue status on official proceedings
pages or publisher sites if the author needs a strict inclusion definition.

## Default venue tiers

### Tier 1 — Top 4 Security Conferences

Include by default:

- `IEEE Symposium on Security and Privacy` (IEEE S&P / Oakland)
- `ACM Conference on Computer and Communications Security` (ACM CCS)
- `Network and Distributed System Security Symposium` (NDSS)
- `USENIX Security Symposium`

These are widely recognized as the four most prestigious cybersecurity venues.

### Tier 2 — Core Security Venues

Include when the scope is `security-all` or broader:

- `Annual Computer Security Applications Conference` (ACSAC)
- `International Symposium on Research in Attacks, Intrusions and Defenses` (RAID)
- `European Symposium on Research in Computer Security` (ESORICS)
- `Privacy Enhancing Technologies Symposium` (PETS)
- `IEEE Computer Security Foundations Symposium` (CSF)
- `ACM Asia Conference on Computer and Communications Security` (AsiaCCS)
- `International Conference on Cryptology and Network Security` (CANS)
- `International Conference on Information Security` (ISC)

### Tier 3 — Broader Security Venues

Include when the scope is `cs-conferences`:

- `Conference on Detection of Intrusions and Malware & Vulnerability Assessment` (DIMVA)
- `Conference on Data and Application Security and Privacy` (DBSec)
- `International Conference on Security and Cryptography` (SECRYPT)
- `SecureComm`
- `Workshop on Privacy in the Electronic Society` (WPES)
- `Workshop on Artificial Intelligence and Security` (AISec)

### Related AI/ML Venues

Include when the scope is `cs-conferences` (for cross-area ML+security work):

- `AAAI Conference on Artificial Intelligence` (AAAI)
- `International Joint Conference on Artificial Intelligence` (IJCAI)
- `Conference on Neural Information Processing Systems` (NeurIPS)
- `International Conference on Machine Learning` (ICML)
- `International Conference on Learning Representations` (ICLR)

### CS/security journals

Include when the scope includes journals:

- `IEEE Transactions on Information Forensics and Security` (IEEE TIFS)
- `IEEE Transactions on Dependable and Secure Computing` (IEEE TDSC)
- `Computers & Security` (Elsevier)
- `ACM Transactions on Privacy and Security` (ACM TOPS)
- `Journal of Computer Security` (JCS)
- `Computers and Security`

## Custom scope

When the user provides a specific venue list, use that list directly. When the user mentions a CORE ranking tier (e.g., CORE A* or A) or CCF level (e.g., CCF-A or CCF-B), map to the corresponding venue list.

## Official source notes

- **CORE rankings** (http://portal.core.edu.au/conf-ranks/) — authoritative Australian conference ranking
- **CCF recommended list** (https://www.ccf.org.cn/) — China Computer Federation recommended venue list
- **DBLP** (https://dblp.org/) — comprehensive CS bibliography with venue metadata
- **IEEE Xplore** (https://ieeexplore.ieee.org/) — IEEE published papers
- **ACM Digital Library** (https://dl.acm.org/) — ACM published papers
- **USENIX** (https://www.usenix.org/publications/proceedings) — USENIX proceedings
- **Crossref REST API** — general scholarly metadata retrieval
- EndNote documents `Reference Manager (RIS)` as an import option for RIS files
