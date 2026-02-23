## System Stability and Performance Analysis:

## Objective:

The system stability and performance analysis features a self-service application workflow with an AWS Lambda backend and Agentic AI that diagnoses issues in real time and suggests fixes. It checks for common problems like network instability, corrupted cache, outdated versions, and expired tokens. RS256 encryption secures logins, while smart session recovery and crash-aware restart maintain user sessions and restore previous states. Key metrics include Crash-Free Sessions Rate (98%+), Login Success Rate (+15%), Average Recovery Time, Automated Issue Resolution Rate (40%+ of incidents), and a 30% reduction in support tickets within 90 days, demonstrating improved reliability, security, and user trust.

## Video of the project:

https://github.com/user-attachments/assets/5a61156f-1fab-4bb8-9324-52b9eafe05a1

## Key Features:

## System Stability and Performance Analysis:

- Continuously monitors app health, detects anomalies, and provides real‑time insights into crashes, slowdowns, and failed user flows.

## “Fix My App” Self‑Diagnostic Workflow.

- A one‑tap troubleshooting system that automatically checks network stability, corrupted cache, outdated app versions, and authentication token issues.

##  AWS Lambda–Powered Backend.

- It is serverless, scalable backend functions that execute diagnostics, automate recovery steps, and ensure fast, cost‑efficient performance under varying load.

## RS256 Secure Authentication.

- All login requests are protected with RS256 encryption to strengthen user identity security, prevent tampering, and ensure safe session handling.

##  Agentic AI Issue Analysis & Recommendations.

- An intelligent agent that analyzes logs, detects root causes, and provides personalized recommendations or automated fixes based on user context.

## Smart Session Recovery.

- Automatically refreshes expired tokens, retries failed logins silently, and restores user sessions without requiring manual re‑authentication.

##  Crash‑Aware Restart.

- After an unexpected crash, the app reopens at the exact page, timestamp, or workflow step the user left off, minimizing disruption.

## KPI‑Driven Reliability Metrics.

-Tracks and reports key performance indicators such as Crash‑Free Sessions Rate, Login Success Rate, Average Recovery Time, Automated Issue Resolution Rate, and Reduction in  Support Tickets.

## Key Installation:

- Ensure you have the following software and frameworks installed.

## Prerequisites:

- Cryptography
- Python
- JSON
- HTML
- RS256 Encrytion
- AWS Cloud Lambda
- LangChain
- LangGraph
- LangSmith
- Gemini 3 Flash
- MCP Server

## Python: Required for all major Component.

- Cryptography
- Python

## RS256 Asymmetric Encryption Setup:

- The prototype uses RS256 asymmetric encryption to secure all authentication flows within the AWS Lambda backend. Login requests are signed with a private RSA key during      JWT generation, while the corresponding public key is used to verify token integrity across services. This ensures that tokens cannot be tampered with, strengthens user      identity protection, and provides a hardened security layer for every login event. The setup aligns with the system’s broader stability framework—supporting secure session   recovery, agentic AI diagnostics, and reliable app performance under real‑world conditions.

## AWS Lambda Installation for Google Colab:

- To support rapid prototyping, the system includes a lightweight setup that allows Google Colab to interact with AWS Lambda. Developers can install the AWS CLI directly in    Colab, authenticate using IAM credentials, and deploy or invoke Lambda functions from the notebook environment. This enables fast iteration on backend logic, real‑time       testing of diagnostic workflows, and smooth integration with the RS256‑secured authentication pipeline.

## LangChain + LangGraph + LangSmith Integration (Prototype Version):

## LangChain — Core Reasoning & Tooling Layer:

## LangChain powers the core reasoning steps of your agent:

- Handles prompt orchestration.
  
- Manages tools (AWS Lambda calls, cache checks, version checks, token validation).
  
- Provides structured outputs for diagnostics.
  
- Integrates with your RS256‑secured authentication flow.
  
## LangGraph — Node‑Based Execution + Fallback Logic:

## Node Examples in the Prototype:

- NetworkCheckNode
  
- CacheCheckNode
  
- VersionCheckNode
  
- TokenValidationNode
  
- CrashRecoveryNode
  
- RecommendationNode (agentic AI)
  
- AWSLambdaInvokeNode

## Each node:

- Runs independently
  
- Passes structured results to the next node
  
- Can trigger fallback paths

## Fallback Logic:

## If a node fails or returns an error:

- NetworkCheckNode → fallback: retry with exponential backoff.
  
- TokenValidationNode → fallback: trigger silent token refresh.
  
- AWSLambdaInvokeNode → fallback: switch to cached local diagnostics.
  
- CrashRecoveryNode → fallback: load last known stable state.
  
LangGraph ensures the workflow never collapses—it simply reroutes.

## LangSmith — Observability, Tracing, and Evaluation:

### LangSmith gives you:

- Full trace logs of each diagnostic step
  
- Node‑level performance metrics
  
- Error clustering
  
- Evaluation of fallback success rates
  
- Insight into agentic reasoning quality
  
## This is essential for your KPIs:
- Automated Issue Resolution Rate
  
- Average Recovery Time
  
- Crash‑Free Sessions Rate
  
## How It All Works Together (Prototype Flow):

- User taps Fix My App
  
- LangGraph starts the diagnostic graph
  
- Each node runs a check (network, cache, version, token, crash state)
  
- LangChain handles reasoning + tool calls
  
- AWS Lambda executes backend checks
  
- RS256‑secured tokens validate identity
  
- Fallback nodes activate if any step fails
  
- Agentic AI generates a recommendation or auto‑fix
  
- LangSmith logs everything for analysis
  
This creates a self‑healing, observable, secure diagnostic system.



















