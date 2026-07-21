# System Architecture

## Overview

The AI Project Planning Engine converts enterprise project documents into explainable project plans.

```
                +----------------------+
                |   User Uploads RFP   |
                +----------+-----------+
                           |
                           v
                +----------------------+
                |  Document Parser     |
                +----------+-----------+
                           |
                           v
                +----------------------+
                | Requirement Extractor|
                +----------+-----------+
                           |
                           v
          +--------------------------------------+
          | AI Orchestrator                      |
          +--------------------------------------+
            |        |        |        |        |
            v        v        v        v        v
      Scope     Risks   Staffing Timeline Cost
      Agent     Agent     Agent     Agent Agent
            \        |        |       /
             \       |        |      /
              +----------------------+
              | Review Agent         |
              +----------+-----------+
                         |
                         v
              +----------------------+
              | Planning Report      |
              +----------------------+
```

---

## Components

### 1. Document Parser

Responsibilities

- Read PDF
- Read DOCX
- Extract clean text
- Preserve headings

---

### 2. Requirement Extractor

Responsibilities

- Functional requirements
- Non-functional requirements
- Constraints
- Deliverables

---

### 3. AI Orchestrator

Responsibilities

- Decide which agents should execute
- Pass context between agents
- Merge outputs

---

### 4. Specialized Agents

Initially

- Scope Agent
- Risk Agent
- Staffing Agent
- Timeline Agent
- Cost Agent

Future

- Security Agent
- Architecture Agent
- Compliance Agent
- Executive Review Agent

---

### 5. Review Agent

Responsibilities

- Detect inconsistencies
- Challenge assumptions
- Improve confidence

---

### 6. Report Generator

Responsibilities

Generate

- Executive Summary
- Scope
- Risks
- Timeline
- Cost
- Assumptions
- Dependencies
- Staffing Plan

---

## Design Principle

Every recommendation produced by AI should include:

- Evidence
- Confidence
- Assumptions
- Reasoning
