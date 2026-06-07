# SOC-7 Threat Intelligence Platform

**Live Demo → [Tommy3714.github.io/soc7-platform](https://Tommy3714.github.io/soc7-platform)**

A fully interactive, enterprise-grade SOC dashboard built from scratch — no frameworks, no templates, no external JavaScript dependencies.

Built by **T.K. Simon** | Security Analyst | Google Cybersecurity Certified

---

## What It Does

SOC-7 simulates a real Security Operations Center workflow from alert ingestion through investigation to case closure. Every button performs a visible action. No placeholder UI.

### Views

| View | What's Inside |
|------|--------------|
| **Overview** | Live metrics derived from alert data, MITRE mini-matrix, event volume chart, recent alerts |
| **Alerts** | Full triage queue — filter by severity/status/keyword, sort by time/host/severity, open detail modal or launch investigation |
| **Investigate** | 7-step workflow: Alert → Host → User → Process Tree → Timeline → Evidence → Remediation |
| **Hunt** | IOC enrichment with confidence scoring, threat actor attribution, MITRE mapping, feed sourcing |
| **Executive** | Enterprise risk score, MTTD/MTTR KPIs, financial exposure ($2.4M model), NIST/SOC2/PCI compliance posture |
| **Cases** | Create, track, and close cases — persisted to localStorage |

### Features
- Alert triage queue with MITRE ATT&CK mapping (T-codes)
- 7-step investigation workflow with per-alert localStorage notes
- IOC enrichment: type, confidence, threat actor, malware family, feed sources, related alerts
- Asset criticality and business impact scoring
- Executive risk view with financial exposure and compliance posture
- Case management that persists across browser sessions
- Mountain Time (MT) native with UTC toggle
- Live log stream, endpoint status panel, geo threat origins
- OWASP Top 10 hardened — zero external JS — all CSP headers set

---

## Security Architecture

| OWASP Control | Implementation |
|---------------|----------------|
| A01 Broken Access | RBAC UI · least privilege · 15min session timer |
| A02 Crypto Failures | AES-256 / TLS 1.3 documented · no plaintext |
| A03 Injection | Central `esc()` sanitizer on all dynamic output · no `eval()` |
| A04 Insecure Design | Threat modeled · no user-controlled DOM injection |
| A05 Misconfiguration | CSP · X-Frame-Options: DENY · X-XSS-Protection · Referrer-Policy |
| A06 Vuln Components | **Zero external JS** — no CDN attack surface |
| A07 Auth Failure | MFA + OAuth 2.0 + OIDC documented · brute force lockout |
| A08 Data Integrity | No innerHTML from unsanitized sources |
| A09 Logging Failure | This platform IS the logging layer |
| A10 SSRF | `connect-src: none` · no user-supplied URLs |

---

## Tech Stack

- **HTML5 / CSS3 / Vanilla JavaScript** — zero build tools
- **Fonts:** Cinzel (headings) · IBM Plex Mono (data) · Barlow (body) via Google Fonts
- **Storage:** localStorage for case persistence and analyst notes
- **Single file** — drop `index.html` anywhere and it runs

---

## Concepts Demonstrated

`SIEM` `IAM` `Incident Response` `Threat Intelligence` `IOC Enrichment` `MITRE ATT&CK` `SOC Operations` `Cyber Risk Management` `OWASP Top 10` `Case Management` `MTTD/MTTR` `Compliance Posture`

---

## About

> I protect systems, data, and people. I'm currently an Administrative Assistant II at the Colorado Department of Revenue, operating inside a state government compliance environment where data integrity and records management are daily requirements — not buzzwords.
>
> SOC-7 is how I close the gap between what I know and what I can show.

**T.K. Simon** · Denver, CO · [LinkedIn](https://www.linkedin.com/in/thomas-simon-64869b382)
