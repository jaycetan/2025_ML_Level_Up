# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Mandatory Agent Rules

**IMPORTANT**: These rules MUST be followed throughout the ENTIRE conversation.

### 1. **CLARIFY FIRST**
Iteratively ask minimal clarifying questions (yes/no or multiple-choice format) before proceeding. Never make assumptions without explicit approval.

### 2. **SYSTEMATIC APPROACH** 
Break down work into clear steps. Use TodoWrite tool for complex tasks. Build incrementally, validate each step.

### 3. **CONTROLLED CHANGES**
Explain how/why/what before executing. Modify only what was agreed upon. Request permission for changes beyond scope.

### 4. **RESEARCH & VERIFY**
Use context7, DuckDuckGo, and project files liberally. Reference official documentation. Verify against multiple sources.

### 5. **MEMORY MANAGEMENT**
Keep memory bank concise and current. Update after completing subtasks. Memory bank location: `.claude/memory-bank/`

---

## Project Overview

**Interview Preparation Framework** for SWE → MLOps/MLE transition

**Daily Practice:**
- 1 Blind 75 algorithm question
- 1 ML system design question  
- 2 Behavioral questions
- 1 ML interview question

**Core Features:**
- Adaptive selection based on performance (1-5 scale)
- Python-only implementation for expertise building
- Daily directories with individual question files
- Performance tracking and analytics

---

## Reference Documents

For detailed information, see:
- **Architecture & Commands:** `.claude/docs/project-architecture.md`
- **Interview Guide & Workflow:** `.claude/docs/interview-prep-guide.md`
- **Memory Bank Prompts:** `.claude/prompts/memory-bank-prompts.md`

---

## Current Focus

Check `.claude/memory-bank/activeContext.md` for latest session state and immediate priorities.