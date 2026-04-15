---
name: repo-onboarding-publisher
description: Analyze a code repository and produce a Markdown onboarding document. Use when asked to inspect a repo, summarize structure and key modules, choose a beginner starting point, explain an example step by step, include a Mermaid diagram, and publish the final onboarding document to Obsidian via MCP.
---

# Repo Onboarding Publisher

Follow this workflow every time.

## Repository Input Rule

- Read from `./moment-develop` by default.
- Use another repository path only when the user explicitly provides one.

## Required Output

- Always produce a Markdown onboarding document.
- Always publish the final document to Obsidian via MCP.

## Required Sections In The Markdown Document

Include all of these sections, with these headings:

1. Overview
2. Structure
3. Key Modules
4. Beginner Starting Point
5. Example Explanation
6. Learning Path
7. Mermaid Diagram

## Workflow

1. Analyze the repository.
- Inspect top-level layout, key modules, stack, entrypoints, and setup/run commands from repository files.

2. Build the onboarding content.
- Write concise, actionable guidance for beginners.
- Keep commands and file references grounded in real repository content.

3. Add a beginner-friendly example.
- Choose one small, representative flow.
- Explain prerequisites, setup, execution, expected result, and code locations step by step.

4. Add a Mermaid diagram.
- Include at least one `flowchart` or `sequenceDiagram` that matches the selected example or module flow.
- Always use quoted Mermaid labels for compatibility:
  - Node labels: `A["Text"]`
  - Decision labels: `B{"Text"}`
  - Edge labels: `-->|"Label"|`
- Avoid unquoted labels when they include punctuation, parentheses, slashes, or line breaks.

5. Publish to Obsidian.
- Write the final Markdown document using Obsidian MCP tools.
- If no destination is provided, publish to `onboarding/<repo-name>-onboarding.md`.
- Confirm the final Obsidian note path in the response.

## Quality Bar

- Base claims on repository files.
- State assumptions clearly.
- Do not invent files, modules, or commands.
