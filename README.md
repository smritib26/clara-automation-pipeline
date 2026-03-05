https://colab.research.google.com/drive/18v1smyh6Hrnby7oHBcVZf1AQKT7-siQb?usp=sharing
# clara-automation-pipeline
Zero-cost automation pipeline for Clara Answers intern assignment
# Clara Answers Automation Pipeline

## Overview
This project implements a zero-cost automation pipeline that processes demo and onboarding call data to generate and update Retell AI agent configurations.

## Architecture
Pipeline A: Demo Call → Preliminary Agent
1. Input: Demo call transcript
2. Extract structured data
3. Generate Account Memo JSON
4. Generate Retell Agent Draft Spec
5. Store outputs

Pipeline B: Onboarding Update
1. Input: Onboarding transcript
2. Update Account Memo
3. Generate new Agent Spec (v2)
4. Store versioned outputs
5. Create changelog

## Output Structure

outputs/
account_001/
v1/
account_memo.json
agent_spec.json

v2/
account_memo.json

changes.json

## Tools Used
- Python
- Google Colab
- JSON storage
- GitHub repository

## Zero-Cost Compliance
No paid APIs or services were used. All processing was done locally using Python.

## Improvements (Future Work)
- Add n8n workflow automation
- Automatic transcript extraction
- Diff viewer for version changes
- Integration with Retell API
