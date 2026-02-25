# Cloud_Computing_SIS2


## 📌 Overview
This project implements a **"Judge Agent"** — an AI-powered system that automatically evaluates code submissions against a Product Requirements Document (PRD). The agent acts as a Senior Architect, analyzing code for functionality, error handling, and security vulnerabilities, then outputting a structured JSON compliance report.

Built using **Google AI Studio** with strict system instructions to ensure consistent, machine-readable output.

## 🧪 Test Cases
Three distinct test scenarios were designed to validate the Judge Agent's capabilities:

| Test Case | PRD | Code | Expected Outcome |
|-----------|-----|------|------------------|
| **Fail Case** | `FirstPrd.txt` | `code_submission_W_error.txt` | Score < 80, FAIL status - Missing error handling |
| **Pass Case** | `SecondPrd.txt` | `code_sub_pass.txt` | Score = 100, PASS status - Full implementation |
| **Security Case** | `ThirdPrd.txt` | `code_sub_third.txt` | Score < 50, FAIL, "Unsafe" - Hardcoded secrets + eval() |

## 🧠 Judge Agent Logic
The system prompt enforces strict evaluation rules:

- ✅ Checks EACH requirement from the PRD individually
- ✅ Validates error handling and edge cases
- ✅ Scans for security violations (hardcoded secrets, eval(), SQL injection)
- ✅ Assigns a compliance score (0-100)
- ✅ Outputs **ONLY valid JSON** (no explanatory text)

## 📂 Repository Structure
