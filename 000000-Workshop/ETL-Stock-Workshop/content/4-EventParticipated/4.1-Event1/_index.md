---
title: "FCAJ Meetup - 13/06/2026"
date: 2026-06-13
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

# FCAJ Meetup - 13/06/2026

## General information

| Item | Information |
|:---|:---|
| Event | FCAJ Meetup |
| Organizer | First Cloud AI Journey (FCAJ) |
| Date | 13/06/2026 |
| Role | Attendee |

The meetup included four complementary perspectives: the work and culture of data analytics in multinational companies, the architecture of a scalable URL shortener on AWS, the real responsibilities of a DevOps engineer, and a development journey from FCAJ to AWS student communities and partner organizations.

## Participation objectives

- Understand the day-to-day work of Data Analytics and DevOps engineers.
- Study how a scalable AWS system is decomposed through the URL Shortener example.
- Learn about recruitment, multinational-company culture, and long-term career development.
- Explore student opportunities such as AWS Student Builder Groups and AWS Community Builders.
- Identify practices that can improve the team's ETL and machine-learning project.

## Speakers and topics

1. **Đạt Phạm and Cường Nguyễn** - real-world Data Analytics work, recruitment, professional development, and multinational-company culture.
2. **Đinh Trung Kiên and Nguyễn Minh Thọ** - *A Scalable URL Shortening Service on AWS*.
3. **Trong H. Truong** - *What Does a DevOps Engineer Really Do?*
4. **Danh Hoàng Hiếu Nghị** - the journey from First Cloud AI Journey to AWS student communities and an AWS Partner environment.

## Key highlights

### Data analytics is more than reporting

A Data Analytics Engineer does not simply calculate indicators and place them on a dashboard. The work requires understanding the business context, monitoring operational performance, detecting anomalies, finding root causes, and communicating a clear data story. When a metric such as GMV changes, reporting the movement is only the first step; the more useful question is why it changed and what action should follow.

The session also highlighted critical thinking, communication, problem solving, and data storytelling. This is directly relevant to the stock dashboard: a collection of charts is not enough if users cannot identify the important signals or understand their limitations.

### A scalable URL Shortener on AWS

The architecture separated responsibilities across CloudFront, AWS WAF, AWS Amplify, containerized services on Amazon ECS, Amazon ElastiCache for Redis, and Amazon DynamoDB. A dedicated Key Generation Service pre-generated short codes, while Redis was used with a cache-aside strategy to reduce repeated database reads.

The most valuable lesson was not the number of AWS services, but the reasoning behind the separation: isolate responsibilities, place caching on read-heavy paths, protect public entry points, and avoid a single component that owns every function.

### DevOps is broader than a tool list

Docker, Kubernetes, CI/CD, and cloud platforms are only parts of DevOps. Strong foundations in Linux, networking, programming, Git, containers, deployment, logging, configuration, and environment variables remain important even as tools change. The message **“Tools change. Fundamentals stay.”** closely reflects the team's experience while changing libraries and deployment approaches during the project.

The session also emphasized asking “why” before “how,” identifying the actual owner of a problem, communicating clearly, and using AI to strengthen thinking rather than replace it.

### From FCAJ to the AWS community

The final session showed that an initial job or training program is only a starting point. FCAJ, AWS Student Builder Groups, AWS Community Builders, and AWS Partner environments can provide opportunities to build projects, share knowledge, meet peers, and gradually create a professional track record. The value depends on sustained learning and contribution rather than participation alone.

## Lessons applied to the project

- Keep ingestion, quality validation, transformation, training, and prediction serving as separate responsibilities.
- Improve logs so each failure identifies the ticker, processing stage, cause, and quarantine location.
- Make the dashboard explain data freshness, quality, and important signals instead of displaying numbers alone.
- Test failure paths by introducing invalid schemas, failed Lambda executions, and erroneous SQS messages.
- Document deployment, IAM permissions, environment variables, and test procedures clearly enough for another member to reproduce the system.

## Reflection

The meetup helped the team connect technology, professional practice, and community development. The immediate priorities are to clarify module boundaries, improve observability, and present the dashboard as a coherent story built from data. The broader lesson is to understand the problem first and then select the smallest set of tools that solves it reliably.
