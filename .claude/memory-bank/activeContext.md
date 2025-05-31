# Active Context

**Last Updated:** 2025-01-30

## Current Session State

### Active Project: Interview Preparation Framework
- **Goal:** Build comprehensive system for daily practice preparing for MLOps/MLE roles
- **Stage:** Core structure complete, ready for implementation
- **Focus:** Created question banks and prompt templates for daily practice

## Immediate Tasks

1. **Completed Today:**
   - ✅ Removed JavaScript implementation (blind-75-js)
   - ✅ Created Python-specific .gitignore
   - ✅ Reorganized CLAUDE.md for efficiency (238→55 lines)
   - ✅ Created question banks with 195 total questions
   - ✅ Built daily practice generator prompt
   - ✅ Built daily review prompt
   - ✅ Moved memory-bank to .claude directory
   - ✅ Analyzed example repos for best practices

2. **Next Steps:**
   - Implement the actual Python scripts for daily generation
   - Create SQLite schema for performance tracking
   - Build the first day's practice session
   - Test the full workflow

## Session Context

### User Requirements (Confirmed)
- Daily practice: 1 Blind 75, 1 ML system design, 2 behavioral, 1 ML interview question
- Adaptive selection based on performance (1-5 grading scale)
- Python-focused implementation for expert-level proficiency
- Daily directory creation with individual files per question
- LLM agent to generate questions and review answers

### Technical Decisions Made
- Simplified approach: avoid over-engineering
- Question banks as JSON files (not scraped, manually curated)
- Two prompts: generator and reviewer for complete learning loop
- Organized .claude directory with docs/, prompts/, question-banks/

## Active Questions/Blockers
- None - ready to implement the Python scripts

## Key Files Modified
- `/CLAUDE.md` - Reorganized with agent rules and references to detailed docs
- `/.claude/memory-bank/` - Moved to .claude directory
- `/.claude/docs/` - Created project architecture and interview guide
- `/.claude/prompts/` - Added daily generator and review prompts
- `/.claude/question-banks/` - Created 4 JSON files with 195 questions
- `/.gitignore` - Replaced Node.js version with Python-specific
- Deleted `/blind-75-js/` directory entirely