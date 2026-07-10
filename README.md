# VERITAS

VERITAS is an enterprise platform for improving the rigor, consistency, and transparency of scientific manuscript review using LLM-assisted workflows. It is designed to support evidence-based auditing across three core scenarios:

- AUTHOR: pre-submission manuscript improvement
- REVIEW: structured peer review and grant critique
- APPRAISE: critical appraisal of published literature

The platform is intended to help authors, reviewers, editors, clinicians, and trainees apply validated research standards more consistently and efficiently.

## Why VERITAS exists

Scientific publishing and review often suffer from inconsistent methodology, weak critical appraisal, and uneven manuscript quality. VERITAS addresses these challenges by operationalizing established review frameworks into a guided workflow that combines AI assistance with structured evidence-based evaluation.

## Core capabilities

- Upload and process manuscripts in common formats such as PDF and DOCX
- Extract manuscript content while preserving structure
- Detect study design and route the review to the appropriate framework
- Apply methodology-aware checks using frameworks such as:
  - ASA p-value guidance
  - CONSORT
  - STROBE
  - Kallogjeri–Piccirillo confidence interval classification
  - ABT narrative framework
- Generate findings with severity levels, evidence citations, and recommendations
- Export polished review reports in Word and PDF formats

## Main modules

### 1. Manuscript ingestion
Supports manuscript upload, text extraction, metadata capture, and preservation of document structure.

### 2. Prompt orchestration
Coordinates multi-step review pipelines, including sequential review workflows and study-aware routing based on manuscript type and design.

### 3. Audit engine
Produces structured findings by applying validated methodological frameworks and classifying issues as Critical, Major, or Minor.

### 4. Reporting
Creates executive summaries, section-wise findings, and downloadable reports for authors and reviewers.

### 5. Identity and security
Provides enterprise-ready access controls, SSO support, institution management, audit logs, and safeguards to keep manuscripts out of model training.

### 6. Analytics
Tracks usage metrics, review turnaround, institutional adoption, and validation outcomes.

## Target users

- Authors who want to improve manuscripts before submission
- Reviewers who need faster, more structured review workflows
- Editors who want consistent quality across reviews
- Clinicians who need tools for critical appraisal
- Trainees who want to learn scientific reasoning and evidence-based evaluation

## MVP scope

The initial product scope includes:

- Authentication
- Manuscript upload
- Review workflow
- Finding generation
- Report generation
- Dashboard experience

## Proposed technical approach

The product is envisioned as a secure, scalable enterprise application with:

- Frontend: Next.js
- Backend: FastAPI or Spring Boot
- Data storage: PostgreSQL and object storage
- AI layer: prompt engine and multi-LLM adapter
- Processing: queue workers and report generation services

## Repository contents

This repository currently includes:

- A prototype UI in index.html
- The product requirements document in Veritas_PRD.md

## Run the prototype locally

A simple local preview can be opened by serving the repository directory:

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000 in your browser.

## Future direction

Planned expansion includes grant review, multilingual support, journal integrations, API access, collaboration features, and custom institutional prompts.
