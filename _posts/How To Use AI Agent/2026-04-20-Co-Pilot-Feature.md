
---
layout: post
title: "How to Use Copilot Perfectly"
date: 2026-04-23
categories: [How To Use AI Agent]
tags: [ai, architecture, voice-agent]
---


---

## INTRODUCTION 

Premium requests — Enterprise plan includes a higher monthly allowance than Business ($19/mo plan). Exact quota set by your admin. Unused requests do NOT roll over each month (reset on the 1st at 00:00 UTC).
Plan	Included models (no cost)	Premium requests	Price
Copilot Enterprise	GPT-4.1, GPT-4o, GPT-5 mini	Higher allowance (set by admin)	$39/user/mo
Copilot Business	Same included models	Lower allowance	$19/user/mo
Context window — Copilot Chat in VS Code supports up to 192k tokens. ~30–40% is reserved for output (system prompt + response buffer), giving you ~100k+ tokens for your actual code and prompts. This is managed on the backend — you cannot configure it.
Premium request multipliers — Advanced models cost more per request. Example: GPT-5 mini = free (included), Claude Sonnet = multiplier ~1x, Claude Opus-class = high multiplier (5–30×). Model choice directly affects how fast you use your monthly allowance.
Usage limits (token-based) — Separate from premium requests. Session + weekly token caps prevent runaway agentic workflows. You can hit a limit even with premium requests remaining. Displayed in VS Code when approaching limits.
---

## CORE VS CODE FEATURE

Inline code completions
Ghost text appears as you type. Tab to accept, Esc to dismiss. Supports all major languages. Unlimited completions on Enterprise.
Always on

Next edit suggestions
Predicts WHERE your next edit will be and suggests it. Goes beyond autocomplete — it follows your intent across files.
VS Code only


Copilot Chat
Full conversational AI in the sidebar. Ask questions, explain code, generate tests, debug errors, architect solutions.
Core feature

Inline chat
Open chat directly inside the editor with Ctrl+I. Ask Copilot to edit selected code without leaving context.
In-editor


Copilot Edits (Edit mode)
Multi-file editing from a single prompt. You choose which files to include and review proposed diffs before accepting.
Granular control

Agent mode
Copilot autonomously decides which files to edit, runs terminal commands, reads outputs, and iterates until the task is done.
Uses most tokens


Agent mode tips — Use for complex refactors, bug fixes that span files, or adding a full feature. Each agent loop can run tools (read files, run tests, edit code). Uses significantly more premium requests — monitor your usage.

---

## Chat Slash Command and Participant 


Command	What it does
/explain	Explains selected code in plain language
/fix	Suggests a fix for bugs or errors in selected code
/tests	Generates unit tests for selected code
/doc	Generates documentation / JSDoc / docstrings
/simplify	Refactors code to be simpler and more readable
/new	Creates a new project or file with a scaffold
/newNotebook	Creates a Jupyter notebook
/terminal	Explains terminal error or suggests a command
/search	Searches your workspace for code matching a description
/setupTests	Sets up a testing framework in your project
Participant (@)	What it does
@workspace	Asks Copilot to reason about your entire codebase
@vscode	Asks about VS Code settings, commands, extensions
@terminal	Explains or generates terminal commands
@github	Asks about GitHub repos, issues, PRs (Enterprise only)


---


## Context Variable(#) 


Variable	What it attaches
#file	Includes a specific file in context
#selection	Includes currently selected code
#editor	Includes all open editor tabs
#codebase	Searches the workspace and includes relevant files (uses @workspace)
#terminalSelection	Includes the selected text from your terminal
#terminalLastCommand	Includes the last terminal command and its output
#problems	Includes errors from the Problems panel
#sym	References a specific symbol (function, class) in your code


=== 


