# Docebo API notes

## Purpose
This skill supports backend and integration work involving Docebo APIs.

## Main reference
- Tenant API explorer:
  `https://merzaestheticsexchange.docebosaas.com/api-browser/`

## What this skill should help with
- Identify relevant endpoints from the tenant API browser
- Explain auth and token requirements
- Propose request / response mappings
- Design backend integration patterns
- Distinguish platform fact from tenant-specific assumption

## Working method
When asked to work with Docebo APIs:
1. Clarify the business goal
2. Identify the Docebo entity involved
3. Identify the endpoint(s)
4. Define auth requirements
5. Define payload shape
6. Define error handling and edge cases
7. Produce an implementation approach

## Output template
Use this format unless the user asks otherwise:

### Objective
What the integration needs to achieve

### Docebo object / area
Users / courses / enrollments / learning plans / content / reports / other

### Endpoint candidate(s)
List relevant endpoint names or API browser paths

### Authentication
Explain token type, backend responsibility, and security implications

### Request / response
Provide example payloads if appropriate

### Risks / assumptions
Call out tenant-specific configuration, permissions, or uncertain areas

### Recommendation
Give the most practical implementation approach

## Rules for the assistant
- Never invent endpoints
- If endpoint certainty is missing, say so explicitly
- Prefer backend orchestration over frontend direct API usage
- Treat the tenant API explorer as the source of truth for available APIs
- Be explicit when the answer depends on tenant permissions or configuration

## Example prompts
- "Design the backend integration to create a user in Docebo and enroll them into a course"
- "Which Docebo API endpoints do I need to retrieve course completion status?"
- "Create a Node.js service layer for Docebo authentication and course enrollment"
- "Map Salesforce contacts to Docebo users"
