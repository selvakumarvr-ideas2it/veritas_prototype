# VERITAS Product Requirements Document (PRD)

## 1. Product Overview
**VERITAS** is an enterprise platform that operationalizes validated scientific-review methodologies through LLM-assisted workflows. Rather than acting as a generic AI writing assistant, VERITAS delivers structured evidence-based audits for scientific manuscripts across three lifecycle stages:
- **AUTHOR** – Pre-submission manuscript improvement
- **REVIEW** – Peer review & grant critique
- **APPRAISE** – Critical appraisal of published literature

## 2. Vision
Become the trusted methodology layer for scientific communication by embedding validated research standards into AI-assisted workflows.

## 3. Problem Statement
Scientific publishing suffers from:
1. Poor manuscript quality
2. Inconsistent peer review
3. Weak critical appraisal

These issues stem from inconsistent application of evidence-based methodology.

## 4. Objectives
- Reduce editorial effort.
- Improve manuscript quality before submission.
- Standardize peer review.
- Improve evidence-based medicine education.
- Enable institutional adoption.

## 5. Target Users
| Persona | Goals |
|---|---|
| Authors | Improve manuscripts before submission |
| Reviewers | Faster structured review |
| Editors | Consistent review quality |
| Clinicians | Critical appraisal |
| Trainees | Learn scientific reasoning |

## 6. Core Modules
### Module 1 – Manuscript Ingestion
- PDF/DOCX upload
- OCR/Text extraction
- Preserve manuscript structure
- Metadata extraction
- Study-design detection

### Module 2 – Prompt Orchestration
- Sequential REVIEW workflow (11 prompts)
- Parallel AUTHOR workflow
- APPRAISE workflow
- Prompt versioning
- Study-aware routing (CONSORT/STROBE)

### Module 3 – Audit Engine
Frameworks:
- ASA p-value guidance
- CONSORT
- STROBE
- Kallogjeri–Piccirillo CI Classification
- ABT Narrative Framework

Outputs:
- Critical/Major/Minor findings
- Evidence citations
- Recommendations

### Module 4 – Reporting
- Word export
- PDF export
- Executive Summary
- Section-wise findings
- Severity dashboard

### Module 5 – Identity & Security
- SSO
- RBAC
- Institution management
- Audit logs
- Manuscripts excluded from model training

### Module 6 – Analytics
- Usage metrics
- Review turnaround
- Institution dashboard
- Validation metrics
- Inter-rater concordance

## 7. Functional Requirements
### Authentication
- SSO
- Email login
- MFA
- RBAC

### Manuscripts
- Upload
- Versioning
- Metadata
- History

### AI Processing
- LLM-agnostic provider abstraction
- Prompt templates
- Pipeline orchestration
- Retry/error handling

### Reports
- Downloadable DOCX/PDF
- Share links
- Comments

## 8. Non-functional Requirements
- SOC2-ready architecture
- Encryption in transit and at rest
- <30 sec ingestion
- Horizontal scalability
- 99.9% uptime
- Full auditability

## 9. High-level Architecture
Frontend:
- Next.js

Backend:
- FastAPI / Spring Boot

Storage:
- PostgreSQL
- Object Storage

AI:
- Prompt Engine
- Multi-LLM Adapter

Processing:
- Queue workers
- Report Generator

## 10. Suggested Data Model
- User
- Institution
- Manuscript
- Audit
- PromptRun
- Finding
- Report
- FrameworkRule

## 11. User Stories
Example:
- As an Author I can upload a manuscript.
- As a Reviewer I can execute an 11-step review.
- As an Editor I can compare review quality.
- As a Clinician I can critically appraise a paper.

## 12. MVP Scope
- Authentication
- Upload
- Review workflow
- Findings
- Report generation
- Dashboard

## 13. Future Releases
- Grant review
- Multi-language
- Journal integrations
- API
- Teams
- Collaboration
- Knowledge graph
- Custom institutional prompts

## 14. KPIs
- Audit completion time
- Report quality
- Reviewer adoption
- Institutional retention
- Prompt accuracy
- User satisfaction

## 15. Revenue Model
1. Journal licensing
2. Academic institutions
3. Individual subscriptions

## 16. Risks
- LLM hallucination
- Regulatory changes
- Publisher integration
- Prompt maintenance

## 17. Success Criteria
- Comparable expert review quality
- Significant reduction in review time
- Institutional adoption
- Secure enterprise deployment
