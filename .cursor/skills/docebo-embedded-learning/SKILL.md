# Docebo Embedded Learning notes

## Purpose
This skill supports frontend and integration work involving embedded learning, widgets, launcher, token handling, and embedded navigation patterns.

## Main references
- Embedded Learning documentation section:
  `https://help.docebo.com/hc/en-us/sections/4407577387026-Embedded-learning`

## What this skill should help with
- Choose between launcher and widget-based embedding
- Define frontend integration pattern
- Define backend token provider requirements
- Explain widget composition
- Explain CSP implications
- Design direct navigation into learning experiences
- Distinguish URL links from launcher/widget navigation

## Working method
When asked to work with embedded learning:
1. Clarify the user journey
2. Decide whether launcher or widgets are the right model
3. Define auth and token flow
4. Define frontend setup
5. Define CSP and security requirements
6. Define navigation approach
7. Produce implementation guidance

## Decision logic
Use this logic by default:

### Use launcher when
- The user wants a broader Docebo experience shell
- Navigation across learning areas is needed
- A popup or contained embedded shell is acceptable
- The goal is faster implementation with platform-native navigation

### Use widgets when
- The user wants tighter UX control
- The learning experience must be embedded inside a custom page layout
- A single course, list, or learning block is needed
- The portal should feel more native than platform-shell-based

## Navigation logic
When the prompt mentions "deep link", determine which one applies:
- Direct platform URL
- Launcher command / launcher opening behavior
- Widget targeting by course / asset / source
- Mobile deep link

Do not mix them.

## Output template
Use this format unless the user asks otherwise:

### Goal
Describe the desired embedded learning journey

### Recommended model
Launcher / widgets / hybrid

### Frontend approach
Scripts, component structure, page placement, state handling

### Backend dependency
Token generation, renewal, proxy, security logic

### Security / CSP
Required allowlists and platform restrictions

### Navigation approach
How the user lands on the correct learning experience

### Constraints / assumptions
Call out tenant-specific dependencies

### Recommendation
Give the most practical solution

## Rules for the assistant
- Never expose secrets in frontend code
- Default to backend token provider pattern
- Flag CSP early
- Do not assume all widgets solve all navigation needs
- Separate UX recommendation from platform limitation
- Keep examples practical and implementation-oriented

## Example prompts
- "Recommend whether we should use launcher or widgets for an HCP portal"
- "Create a React integration pattern for Docebo embedded learning"
- "Embed a course player for one specific course in our portal"
- "Design the token renewal flow for embedded learning"
- "Explain how to open the embedded learning experience directly to a relevant learning context"
