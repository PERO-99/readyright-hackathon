# ReadyRight – System Design

## Architecture Overview

User Interface  
→ API Gateway  
→ AWS Lambda  
→ Eligibility Logic Engine  
→ Amazon Bedrock (AI reasoning)  
→ Scheme Rule Database  
→ Readiness Verdict

---

## Data Layer

Structured scheme database containing:

- eligibility rules
- required documents
- thresholds
- official references
- update timestamp

Data is sourced from public government information and verified before ingestion.

---

## AI Layer

AI interprets structured rules and generates:

- readiness prediction
- missing requirement explanation
- human-readable guidance

AI does not invent rules. It reasons over verified data.

---

## Update Pipeline

- Scheduled ingestion job
- Rule change detection
- Human validation step
- Database update
- Version tracking

Accuracy prioritized over automation.

---

## Security Design

- No persistent storage of personal identifiers
- Session-based processing
- Consent-driven interaction
- Minimal data retention

---

## Scalability

Serverless architecture allows:

- on-demand scaling
- low operational cost
- easy deployment across regions

