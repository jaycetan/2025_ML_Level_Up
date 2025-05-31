# Active Context

**Last Updated:** 2025-01-30 (Evening Session)

## Current Session State

### Active Project: Interview Preparation Framework
- **Goal:** Build comprehensive system for daily practice preparing for MLOps/MLE roles
- **Stage:** Netflix interview prep integration complete
- **Focus:** Created comprehensive Netflix recruiter interview preparation system

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

2. **Completed This Session:**
   - ✅ Created Netflix-specific recruiter interview question bank
   - ✅ Built document-based coaching prompt for practice sessions
   - ✅ Researched Netflix culture memo and job description integration
   - ✅ Prepared Jayce for upcoming recruiter call with Alice Chiang

3. **Next Steps:**
   - Generate first Netflix practice session document
   - Continue with general interview prep framework implementation
   - Create SQLite schema for performance tracking

## Session Context

### User Requirements (Confirmed)
- **General Prep**: Daily practice with 1 Blind 75, 1 ML system design, 2 behavioral, 1 ML interview question
- **Netflix Specific**: Recruiter interview preparation for ML Software Engineer role
- **Adaptive selection** based on performance (1-5 grading scale)
- **Python-focused** implementation for expert-level proficiency
- **Document-based coaching** for Netflix interview practice
- **LLM agents** to generate questions and provide detailed feedback

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
- `/.claude/netflix_prep/` - Netflix-specific interview preparation materials
- `/.claude/prompts/netflix-recruiter-coach.md` - Document-based coaching system