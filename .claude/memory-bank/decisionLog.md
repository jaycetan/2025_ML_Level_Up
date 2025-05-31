# Decision Log

**Project:** Interview Preparation Framework for MLOps/MLE Transition

## Technical Decisions

### 2025-01-30: Project Architecture

#### Decision: Python-Based Implementation
**Choice:** Python as sole implementation language
**Rationale:**
- MLOps/MLE roles require expert Python proficiency
- Ensures daily practice with Python idioms and best practices
- Aligns with ML ecosystem (scikit-learn, PyTorch, TensorFlow)
- Better preparation for technical interviews in target roles

**Alternatives Considered:**
- JavaScript/TypeScript - Rejected: Not primary language for ML roles
- Mixed stack - Rejected: Focus on Python mastery is priority

#### Decision: Adaptive Question Selection
**Choice:** Performance-based algorithm with 1-5 grading scale
**Rationale:**
- Focuses practice on weak areas
- Prevents wasting time on mastered concepts
- Provides measurable progress tracking
- Mimics spaced repetition learning

**Implementation Details:**
- Weight questions by inverse of average score
- Increase probability for topics with scores < 3
- Ensure coverage of all categories over time

#### Decision: Directory-Based Daily Structure
**Choice:** `/daily-sessions/YYYY-MM-DD/` with individual files
**Rationale:**
- Clear organization and history
- Easy to review past sessions
- Git-friendly for tracking progress
- Allows focused work on each question type

**File Structure:**
- `blind75.py` - Algorithm implementation
- `ml-system-design.md` - Design documentation
- `behavioral-[1-2].md` - STAR format responses
- `ml-interview.py` - Theory + implementation

#### Decision: SQLite for Performance Tracking
**Choice:** SQLite database for scores and analytics
**Rationale:**
- Lightweight, no server required
- Perfect for single-user application
- Easy to query for analytics
- Portable and version-controllable

**Schema Considerations:**
- Track date, question_id, category, score, time_spent
- Enable trend analysis and weak area identification

#### Decision: LLM-Powered Question Generation and Review
**Choice:** Two comprehensive prompts for daily generation and review
**Rationale:**
- Generate fresh, contextual questions daily
- Provide objective feedback and grading (1-5 scale)
- Avoid maintaining large static question databases
- Enable adaptive difficulty based on performance

**Implementation Details:**
- daily-interview-prep-generator.md: Creates complete daily sessions
- daily-interview-review.md: Reviews answers with detailed feedback
- Both prompts reference question bank JSON files for structure
- Follow prompt engineering best practices from guide

#### Decision: Avoid Over-Engineering
**Choice:** Rejected complex spaced repetition algorithms and web frameworks
**Rationale:**
- User would spend more time building than practicing
- Simple JSON files + prompts achieve 80% of value with 20% effort
- Can add complexity later if needed
- Focus on actual interview preparation, not tool building

#### Decision: Comprehensive Question Banks
**Choice:** Created 4 JSON files with 195 curated questions
**Rationale:**
- Provides structure for LLM generation
- Ensures comprehensive coverage of all topics
- Easy to track which questions have been used
- Can expand or modify as needed

**Content:**
- blind75.json: 75 algorithm problems with categories
- ml-system-design.json: 35 company scenarios with constraints
- behavioral.json: 45 questions across competencies
- ml-theory.json: 40 ML concepts with MLOps connections

## Architectural Principles

1. **Simplicity First:** Avoid over-engineering, focus on daily usability
2. **Python Excellence:** Every solution demonstrates best practices
3. **Data-Driven:** Let performance metrics guide learning path
4. **Comprehensive Coverage:** Balance all interview aspects equally
5. **LLM-Powered:** Use AI for generation and review, not just storage
6. **Iterative Improvement:** Start simple, add complexity when needed