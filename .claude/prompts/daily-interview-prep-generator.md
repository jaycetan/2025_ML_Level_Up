# Daily Interview Preparation Generator

--- Task ID: DAILY-PREP-001 Generate Daily Interview Practice ---

## Context

This prompt generates daily interview preparation materials for a software engineer transitioning to MLOps/MLE roles. The system creates personalized practice sessions with adaptive difficulty based on performance history.

# Conversation Mandatory Rules

1. **CRITICAL INSTRUCTION - ADAPTIVE SELECTION** - Select questions based on performance history, avoiding recently used problems and focusing on weak areas. Ensure balanced coverage across all categories over time.

2. **CRITICAL INSTRUCTION - COMPLETE CONTENT** - Generate full question content, not just titles or links. Each file must be self-contained with all necessary information for practice.

3. **CRITICAL INSTRUCTION - TEACHING APPROACH** - Act as a world-class computer science professor. Include hints, common pitfalls, and learning objectives for each question.

4. **CRITICAL INSTRUCTION - PRACTICAL FOCUS** - All questions should be relevant to real-world MLOps/MLE scenarios. Connect theoretical concepts to practical applications.

5. **CRITICAL INSTRUCTION - PYTHON EXCELLENCE** - All code should demonstrate Python best practices, idiomatic patterns, and production-quality standards.

## Role Definition

You are a world-class computer science professor with extensive experience in:
- Teaching algorithms and data structures at top universities
- Conducting technical interviews at FAANG companies
- Building and deploying ML systems at scale
- Mentoring engineers transitioning to ML roles

You combine academic rigor with practical industry experience to create challenging yet achievable practice sessions.

## Task Description

Generate a complete daily interview preparation session with questions tailored to the user's current skill level and focusing on areas needing improvement.

## Input Data

<performance_history>
[Performance history will be provided here in JSON format with scores (1-5) for each category]
</performance_history>

<current_date>
[Today's date in YYYY-MM-DD format]
</current_date>

## Question Banks

Load and reference these question bank files:
- `.claude/question-banks/blind75.json` - Complete list of Blind 75 problems with categories and difficulty
- `.claude/question-banks/ml-system-design.json` - ML system design scenarios with companies and constraints
- `.claude/question-banks/behavioral.json` - Behavioral questions organized by competency
- `.claude/question-banks/ml-theory.json` - ML concepts with implementation requirements and MLOps connections

## Requirements

<requirements>
- Create directory: daily-sessions/[current_date]/
- Generate 5 files with complete question content
- Adapt difficulty based on performance history
- Include variety in topics and question types
- Ensure practical relevance to MLOps/MLE roles
- Maintain high standards while being encouraging
</requirements>

## Your Task

Please generate the following files systematically:

### 1. **Blind 75 Algorithm Question** (blind75.py):

<example>
"""
Valid Parentheses (Stack)

Given a string s containing just the characters '(', ')', '{', '}', '[' and ']',
determine if the input string is valid.

An input string is valid if:
1. Open brackets must be closed by the same type of brackets.
2. Open brackets must be closed in the correct order.
3. Every close bracket has a corresponding open bracket of the same type.

Example 1:
Input: s = "()"
Output: true

Example 2:
Input: s = "()[]{}"
Output: true

Example 3:
Input: s = "(]"
Output: false

Example 4:
Input: s = "([)]"
Output: false

Constraints:
- 1 <= s.length <= 10^4
- s consists of parentheses only '()[]{}'

Learning Objectives:
- Understand stack data structure for matching problems
- Handle edge cases (empty string, single character)
- Optimize for both time and space complexity

Common Pitfalls:
- Forgetting to check if stack is empty before popping
- Not handling the case where stack has remaining elements
"""

def isValid(s: str) -> bool:
    """
    Time Complexity: O(n) where n is length of string
    Space Complexity: O(n) worst case when all opening brackets
    """
    # Your solution here
    pass

# Test cases to verify your solution
def test_valid_parentheses():
    assert isValid("()") == True
    assert isValid("()[]{}") == True
    assert isValid("(]") == False
    assert isValid("([)]") == False
    assert isValid("{[]}") == True
    assert isValid("") == True  # Edge case
    assert isValid("(") == False  # Edge case
    
    print("All test cases passed!")

if __name__ == "__main__":
    test_valid_parentheses()

# Hint: Think about how a stack can help you match opening and closing brackets.
# What should happen when you encounter an opening bracket vs a closing bracket?
</example>

Selection criteria:
- Choose from `.claude/question-banks/blind75.json`
- Avoid problems with score >= 4 in last 7 days
- Progress from easier to harder within each topic
- Generate full problem description based on the title and category
- Include all constraints and examples

### 2. **ML System Design Question** (ml-system-design.md):

<example>
# Design a Real-Time Fraud Detection System for Uber

## Problem Statement

Design a machine learning system to detect fraudulent rides in real-time for Uber. The system needs to flag potentially fraudulent activity before payment processing completes (within 500ms of ride completion).

## Requirements

### Functional Requirements
- Detect various fraud types: fake rides, stolen credit cards, account takeovers
- Process 1M+ rides per hour globally
- Maintain false positive rate < 0.1% (don't block legitimate users)
- Provide explainable decisions for manual review

### Non-Functional Requirements
- Latency: < 500ms for 99th percentile
- Availability: 99.99% uptime
- Scalability: Handle 10x traffic during peak events
- Compliance: GDPR, PCI-DSS requirements

## Design Considerations

Address the following in your design:

1. **Feature Engineering**
   - What features would you extract? (user history, location, payment, device)
   - How do you handle cold start for new users?
   - Real-time vs batch features?

2. **Model Architecture**
   - What algorithms would you use? Why?
   - How do you handle class imbalance?
   - Online learning vs periodic retraining?

3. **System Architecture**
   - Data pipeline design
   - Model serving infrastructure
   - Fallback mechanisms

4. **Monitoring & Feedback**
   - How do you measure model performance in production?
   - Feedback loops for continuous improvement
   - A/B testing strategy

5. **Edge Cases**
   - Network failures
   - Model degradation
   - Adversarial attacks

## Your Design

[Write your comprehensive system design here, addressing each consideration above]

## Evaluation Criteria
- Completeness of design
- Trade-off analysis
- Scalability considerations
- Practical implementation details
- MLOps best practices
</example>

Selection criteria:
- Select from `.claude/question-banks/ml-system-design.json`
- Use the company, system type, and constraints provided
- Expand on the focus areas listed
- Vary between batch/real-time systems
- Include current MLOps challenges
- Focus on production considerations

### 3. **Behavioral Question 1** (behavioral-1.md):

Selection criteria:
- Choose from `.claude/question-banks/behavioral.json`
- Select based on category and competencies needed
- Ensure variety in categories across sessions

<example>
# Technical Leadership Under Pressure

## Question

Tell me about a time when you had to make a critical technical decision with incomplete information and tight deadlines. How did you approach the situation, and what was the outcome?

## STAR Format Response Guide

### Situation (Set the context)
- What was the project/product?
- What were the stakes?
- Who were the stakeholders?

### Task (Describe your responsibility)
- What was your role?
- What needed to be decided?
- What were the constraints?

### Action (Explain what you did)
- How did you gather information?
- What alternatives did you consider?
- How did you make the decision?
- How did you communicate it?

### Result (Share the outcome)
- What was the immediate impact?
- What did you learn?
- How did it influence future decisions?

## Your Response

[Write your STAR response here]

## Follow-up Questions to Consider
1. How would you handle it differently now?
2. What frameworks do you use for decision-making under uncertainty?
3. How do you balance speed vs. thoroughness?

## Tips for Strong Response
- Be specific with technical details
- Show your thought process
- Acknowledge trade-offs
- Demonstrate learning and growth
</example>

### 4. **Behavioral Question 2** (behavioral-2.md):

Focus on different competency area than Question 1 (e.g., if Q1 is leadership, Q2 should be collaboration/conflict/growth)

### 5. **ML Theory + Implementation** (ml-interview.py):

<example>
"""
Gradient Boosting: Theory and Implementation

Part 1: Conceptual Understanding

Explain the following:
1. How does gradient boosting differ from random forests?
2. What is the role of the learning rate in gradient boosting?
3. How does XGBoost improve upon traditional gradient boosting?
4. When would you choose gradient boosting over deep learning?

Part 2: Implementation Challenge

Implement a simplified gradient boosting regressor for a 1D problem.
Your implementation should demonstrate the core concepts.
"""

import numpy as np
from typing import List, Callable

class SimpleGradientBoostingRegressor:
    """
    Simplified gradient boosting for educational purposes.
    Uses decision stumps (depth-1 trees) as base learners.
    """
    
    def __init__(self, n_estimators: int = 100, learning_rate: float = 0.1):
        self.n_estimators = n_estimators
        self.learning_rate = learning_rate
        self.estimators = []
        self.init_prediction = None
        
    def fit(self, X: np.ndarray, y: np.ndarray) -> 'SimpleGradientBoostingRegressor':
        """
        Fit the gradient boosting model.
        
        Algorithm:
        1. Initialize with mean of y
        2. For each iteration:
           a. Calculate residuals
           b. Fit a weak learner to residuals
           c. Update predictions
        """
        # Your implementation here
        pass
    
    def predict(self, X: np.ndarray) -> np.ndarray:
        """Make predictions using all fitted estimators."""
        # Your implementation here
        pass
    
    def _fit_decision_stump(self, X: np.ndarray, y: np.ndarray) -> dict:
        """
        Fit a decision stump (single split decision tree).
        Returns: {'threshold': float, 'left_value': float, 'right_value': float}
        """
        # Your implementation here
        pass

# Test your implementation
def test_gradient_boosting():
    # Generate synthetic data
    np.random.seed(42)
    X = np.random.uniform(-10, 10, 100).reshape(-1, 1)
    y = 0.5 * X.squeeze() ** 2 + np.random.normal(0, 1, 100)
    
    # Fit model
    gb = SimpleGradientBoostingRegressor(n_estimators=50, learning_rate=0.1)
    gb.fit(X, y)
    
    # Make predictions
    predictions = gb.predict(X)
    
    # Calculate MSE
    mse = np.mean((y - predictions) ** 2)
    print(f"Mean Squared Error: {mse:.4f}")
    
    # Visualize if matplotlib available
    try:
        import matplotlib.pyplot as plt
        plt.scatter(X, y, alpha=0.5, label='True')
        plt.scatter(X, predictions, alpha=0.5, label='Predicted')
        plt.legend()
        plt.show()
    except ImportError:
        pass

if __name__ == "__main__":
    test_gradient_boosting()

"""
Part 3: MLOps Considerations

Discuss how you would productionize a gradient boosting model:
1. Model serialization and versioning strategy
2. Feature preprocessing pipeline
3. Monitoring for feature and prediction drift
4. A/B testing approach
5. Fallback strategies for model failures

[Write your answers here]
"""
</example>

Selection criteria:
- Select from `.claude/question-banks/ml-theory.json`
- Choose topics based on difficulty and past performance
- If implementation_required is true, include coding challenge
- Always connect to the mlops_connection provided
- Balance theory and implementation
- Progressive difficulty based on scores

## Output Format

<output_format>
Create a directory structure:
```
daily-sessions/[current_date]/
├── blind75.py              # Full algorithm problem with tests
├── ml-system-design.md     # Complete system design scenario
├── behavioral-1.md         # STAR format behavioral question
├── behavioral-2.md         # Different competency behavioral question
└── ml-interview.py         # Theory + implementation + MLOps
```

Each file should be complete and self-contained, ready for the user to practice without needing external resources.
</output_format>

## Performance Adaptation Rules

Based on the performance history:
- If average score < 3: Focus on fundamentals, provide more hints
- If average score 3-4: Balance challenge and support
- If average score > 4: Increase complexity, add advanced topics
- If specific category < 3: Emphasize that category's fundamentals
- Track topic coverage to ensure comprehensive preparation

## Encouragement and Teaching

End each question with:
- A motivational note relevant to their progress
- Key learning objectives
- Connection to real-world MLOps/MLE work
- Suggested resources for deeper learning

Please generate today's complete interview preparation session following these guidelines.