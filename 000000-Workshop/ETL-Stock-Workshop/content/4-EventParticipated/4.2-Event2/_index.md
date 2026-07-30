---
title: "Agentic AI Build Week - 25/07/2026"
date: 2026-07-25
weight: 2
chapter: false
pre: " <b> 4.2. </b> "
---

# Agentic AI Build Week - Project Sharing & Hackathon Journey

## General information

| Item | Information |
|:---|:---|
| Event | Agentic AI Build Week - Project Sharing & Hackathon Journey |
| Organizer | First Cloud AI Journey / Agentic AI Build Week |
| Date | 25/07/2026 |
| Role | Attendee |

The event presented three different journeys in building Agentic AI products under practical constraints. SignalScout and Plan V demonstrated completed prototypes, while team 3KA shared an honest account of a 24-hour hackathon, including scope decisions, technical failures, collaboration issues, and demo preparation.

## Participation objectives

- Learn how teams convert an Agentic AI idea into a demonstrable product.
- Review AWS architectures that coordinate agents and multiple data sources.
- Understand the importance of evidence, explainability, and human oversight in AI-assisted decisions.
- Learn how to control scope, divide work, and prepare a reliable demo under tight time constraints.
- Identify lessons applicable to the team's ETL and stock-movement classification project.

## Teams and solutions

### SignalScout

SignalScout detects early signals of changes in corporate strategy. It gathers information from distributed sources, checks supporting evidence, analyzes indicators, and organizes the findings into a traceable narrative for strategy, risk, competitive-intelligence, and B2B customer teams. The output supports human decisions such as **Maintain**, **Adapt**, or **Accelerate** rather than making the final decision automatically.

Its architecture combined Route 53, Amplify, WAF, Cognito, API Gateway, Lambda, AgentCore Runtime, AgentCore Memory, Strands Agent, Amazon Bedrock Guardrails, S3, DynamoDB, CloudWatch, CloudTrail, IAM, and Secrets Manager. Separate crawler and analysis subagents illustrated how responsibilities can be divided. The team also presented a lower-cost alternative using AgentCore Gateway with web-search and browser tools, showing that architecture should evolve after reviewing cost, dependencies, and observability.

### Plan V - Solution Architect Professional AI Native App

Plan V addressed the time required for Solution Architects to read requirements, identify missing information, draft architectures, draw diagrams, and estimate AWS costs. The application accepts structured documents or natural-language input, builds a Requirements Catalogue, proposes high-level architecture options, produces editable Draw.io diagrams, and creates an indicative cost estimate for `ap-southeast-1`.

The workflow used an internal knowledge base, Amazon Bedrock, Draw.io MCP, and AWS Pricing MCP. The implementation separated the frontend, backend, agent, project data, and AI services with S3, CloudFront, Cognito, an Application Load Balancer, ECS Fargate, PostgreSQL, EFS, ECR, CloudWatch, and Terraform. The most important design choice was to call the results **draft outputs**: AI reduces repetitive work and provides a starting point, while the Solution Architect still validates assumptions, security constraints, and the final design.

### Team 3KA - S.H.E.P.H.E.R.D.

S.H.E.P.H.E.R.D. stands for *Smart Human-flow Evaluation, Prediction, Hazard Detection, Response, and Dispatch*. The system processes camera feeds to track people, measure crowd density, estimate queue conditions, identify congestion risks, create alerts, and suggest operational actions.

The computer-vision layer used YOLO and ByteTrack with Kinesis Video Streams, ECS, a SageMaker Endpoint, DynamoDB, and S3. The web layer used CloudFront, API Gateway, Lambda, and Cognito. AgentCore Runtime, Strands Agent, Amazon Bedrock, and AgentCore Memory provided two roles: an **Autonomous Monitor** for proactive observation and an **Operator Copilot** for natural-language questions.

The team's 24-hour journey also exposed practical risks: unstable code, inference latency, unclear role ownership, lack of sleep, missed commits, and accidentally pushing an environment file. Their recommendations were to define “done,” prepare accounts and starter templates, assign clear roles, reduce scope, and rehearse a short demo story.

## Key lessons learned

### Start with the decision or problem

Each project began with a concrete need: detect strategic change, accelerate architecture drafting, or help operators monitor crowded locations. The stock project should likewise explain what users gain from the pipeline, Quality Gate, classification model, and dashboard instead of describing the project only as a collection of AWS services.

### AI needs evidence and human checkpoints

SignalScout linked conclusions to evidence, while Plan V treated its architecture as a draft for professional review. The stock-direction classifier should also be presented as decision-support information, not guaranteed investment advice. Users need the input data, update time, quality status, important features, and model limitations.

### Control scope before adding features

A small end-to-end flow that works reliably is more valuable than many unfinished features. The team should stabilize data ingestion, validation, transformation, inference, and visualization for a clear set of tickers before introducing additional models or an Agentic AI layer.

### Consider cost, security, and observability early

The presentations repeatedly included authentication, secret management, monitoring, and cost. The current project should track Lambda invocations, S3 storage, SQS failures, API usage, and unexpected expenses; sensitive values must remain outside Git and be managed through environment variables or Secrets Manager where appropriate.

### Team practices affect the demo

Branch conventions, clear ownership, internal deadlines, and a fallback demo are as important as the model. A verified dataset, sample inference result, and dashboard screenshots should be available if the live API or network fails.

## Planned application to the stock project

- Rewrite the project value proposition around data trust, interpretable signals, and decision support.
- Display evidence alongside predictions: input date, quality-check status, and key features.
- Keep a human review step and clearly state that outputs are for reference only.
- Prioritize a stable minimum viable end-to-end flow before expanding scope.
- Separate collection, validation, feature transformation, training, inference, and visualization.
- Monitor costs and errors, and strengthen secret-management and Git practices.
- Assign clear demo roles and prepare a tested fallback scenario.

## Reflection

The event showed that an AI product is not created by selecting a model or calling an API alone. Problem definition, data organization, evidence, cost control, security, and team coordination determine whether the result is useful. The team will first improve the reliability and explainability of the current pipeline; an assistant or agent may be considered later only when the foundation is stable.
