# Memory Bank Prompts

## Initialize Memory Bank

**Use when:** Starting new project or establishing memory bank for existing project

```
Create a memory bank system for this project. Initialize a `.claude/memory-bank/` directory with these core files:

**Files to Create:**
- `activeContext.md` - Current session state, goals, immediate focus
- `decisionLog.md` - Technical decisions, architectural choices, rationale  
- `progress.md` - Completed work, current tasks, upcoming milestones

**Instructions:**
1. Analyze current project structure and codebase
2. Use existing `projectBrief.md` if present for context
3. Populate each file with relevant initial content
4. Include clear purpose statements and consistent markdown structure
5. Cross-reference files where appropriate
6. Add timestamps and logical sections

Provide summary of initialization and suggest next steps.
```

## Update Memory Bank

**Use when:** End of sessions, after major changes, preserving latest context

```
Update the memory bank with our latest session context and developments.

**Update Process:**
1. Analyze recent conversation and code changes
2. Identify key information to preserve
3. Update relevant files while maintaining structure
4. Add timestamps to new entries
5. Ensure cross-file consistency

**Capture These Areas:**
- New features implemented/planned
- Bug fixes and reasoning
- Architecture changes
- Performance optimizations
- Emerging code patterns
- Lessons learned/insights
- Blockers and solutions
- Testing approaches

**Files to Update:**
- `activeContext.md` - Current goals, recent decisions, immediate focus
- `decisionLog.md` - New technical decisions, design rationale
- `progress.md` - Completed tasks, current status, next priorities  

Summarize key updates and recommend next session priorities.
```

## Load Memory Bank Context

**Use when:** Starting new session, refreshing context, onboarding to existing project

```
Load and absorb the memory bank context to understand the current project state.

**Process:**
1. Read all memory bank files in this order:
   - `decisionLog.md` - Past technical decisions and rationale
   - `progress.md` - Current status and completed work
   - `activeContext.md` - Latest session state and immediate goals

2. Analyze and synthesize the information to understand:
   - Project purpose, scope, and requirements
   - Technical architecture and key decisions
   - Current development status and priorities
   - Established patterns and coding standards
   - Recent context and active focus areas

3. Provide comprehensive summary covering:
   - **Project Overview** - What this project does and why
   - **Current State** - Where we are in development
   - **Active Goals** - What we're working on now
   - **Key Patterns** - Important standards to follow
   - **Recent Decisions** - Latest technical choices made
   - **Next Steps** - Recommended priorities

4. Confirm context absorption and readiness to continue development with full project understanding.

Output: "Memory bank context loaded. Ready to continue development with full project understanding."
```

## Quick Commands

**Initialize:** Copy "Initialize Memory Bank" prompt to Claude Code CLI
**Update:** Copy "Update Memory Bank" prompt to Claude Code CLI
**Load Context:** Copy "Load Memory Bank Context" prompt to Claude Code CLI  
**Manual Sync:** Use "UMB" or "update memory bank" as fallback command