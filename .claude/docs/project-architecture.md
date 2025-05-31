# Project Architecture

## Project Structure

```
/interview-prep/
├── daily-sessions/         # Daily quiz directories (YYYY-MM-DD format)
│   └── 2025-01-30/
│       ├── blind75.py      # Algorithm question of the day
│       ├── ml-system-design.md
│       ├── behavioral-1.md
│       ├── behavioral-2.md
│       └── ml-interview.py
├── question-banks/         # Question repositories
│   ├── blind75/           # Python implementations
│   ├── ml-system-design/  
│   ├── behavioral/
│   └── ml-interview/
├── performance/           # Tracking and analytics
│   ├── scores.json       # Daily scores (1-5 scale)
│   ├── analytics.py      # Performance analysis
│   └── visualizations/   # Progress charts
├── quiz-system/          # Core quiz functionality
│   ├── generator.py      # Adaptive question selection
│   ├── grading.py        # Scoring rubrics
│   └── daily-setup.py    # Automated directory creation
└── tests/               # Unit tests for all components
```

## Technology Stack

- **Python 3.9+**: All implementations
- **pytest**: Testing framework
- **pandas/numpy**: Data analysis
- **matplotlib/seaborn**: Visualizations
- **pydantic**: Data validation
- **SQLite**: Performance data storage

## Development Commands

```bash
# Create daily session
python quiz-system/daily-setup.py

# Run tests
pytest tests/ -v --cov=.

# Generate performance report
python performance/analytics.py

# Lint code
pylint **/*.py

# Format code
black .
```