# Alibaba Cloud Deployment Proof

This document describes the Alibaba Cloud deployment plan and current Qwen Cloud integration status for **HydroCompute: Sentinel**.

HydroCompute: Sentinel is currently in local prototype/demo mode. The project is prepared for Alibaba Cloud deployment, but a live Alibaba Cloud backend endpoint has not yet been completed.

---

## Current Status

**Status:** Deployment pending  
**Current runtime:** Local Python prototype  
**Qwen Cloud integration:** Prepared through OpenAI-compatible configuration  
**Backend cloud deployment:** Pending  
**Proof evidence:** To be added after deployment and API test

---

## Deployment Pattern

HydroCompute: Sentinel is designed to be deployed on Alibaba Cloud using one of the following backend patterns:

* **Alibaba Cloud Function Compute** for a lightweight serverless API deployment
* **Elastic Compute Service (ECS)** for a standard Python backend deployment
* **Container Service for Kubernetes (ACK)** for a containerized deployment path

The intended backend workflow is:

```text
Scenario Input
→ Deterministic Python Risk Scoring
→ Qwen Cloud Reasoning
→ Stakeholder Reports
→ Human Approval Gate
```

---

## Qwen Cloud Configuration

HydroCompute uses Qwen Cloud as the reasoning and reporting layer through the OpenAI-compatible Qwen endpoint.

```env
QWEN_API_KEY=your_qwen_cloud_key_here
QWEN_BASE_URL=https://dashscope-intl.aliyuncs.com/compatible-mode/v1
QWEN_MODEL=qwen-plus
```

The Qwen layer is used for:

* contradiction detection
* missing-data explanation
* regulator-facing readiness notes
* public civic impact brief generation
* developer mitigation language
* human-review checklist generation

Qwen Cloud does **not** calculate or override deterministic risk scores.

---

## Environment Variables

Production deployment should configure these variables in the Alibaba Cloud runtime environment:

```env
QWEN_API_KEY=
QWEN_BASE_URL=https://dashscope-intl.aliyuncs.com/compatible-mode/v1
QWEN_MODEL=qwen-plus
```

No API keys, tokens, or secrets should be committed to GitHub.

---

## Deployment Steps

Planned deployment process:

1. Prepare Python environment from `requirements.txt`.
2. Configure Qwen environment variables in Alibaba Cloud.
3. Deploy the backend API or CLI runner to Alibaba Cloud.
4. Run a test scenario through the deployed backend.
5. Confirm that deterministic scoring executes successfully.
6. Confirm that Qwen Cloud generates the reasoning/reporting output.
7. Capture proof through a screenshot, log, or screen recording.
8. Add the deployed endpoint and proof evidence to this document.

---

## Evidence To Add After Deployment

After deployment is complete, add:

* Alibaba Cloud service name
* Runtime used: Function Compute, ECS, or ACK
* Deployment region
* Backend endpoint URL
* Screenshot or screen recording of Alibaba Cloud console
* Successful test request or CLI output
* Confirmation that secrets are stored only as environment variables
* Confirmation that no `.env` file or API key is committed to GitHub

---

## Current Proof Status

Alibaba Cloud backend deployment has not yet been completed.

Current proof consists of:

* Qwen-compatible environment configuration
* OpenAI-compatible Qwen API pattern in project documentation
* Local deterministic scoring workflow
* Local demo workflow prepared for Qwen-powered reasoning

This document will be updated after the first successful Alibaba Cloud deployment and Qwen test run.

---

## Compliance and Safety Notes

* HydroCompute: Sentinel is a prototype decision-support system.
* Outputs are draft artifacts requiring human review.
* The system does not issue legal, engineering, environmental, financial, regulatory, or permitting determinations.
* Qwen Cloud is used for reasoning, explanation, contradiction detection, and stakeholder report drafting.
* Deterministic Python code remains the authoritative scoring layer.
* Sentinel QC Water Node is a simulator, not a real deployed hardware device.

---

*HydroCompute: Sentinel | Alibaba Cloud Deployment Proof*
*Deployment pending. Draft decision-support artifact requiring human review.*
