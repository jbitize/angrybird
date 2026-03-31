# CLAUDE.md

## Workflow Rules

### 1. No Implementation Without Approval
- When the user describes a problem or requirement, **DO NOT implement immediately**.
- Always ask "구현할까요?" and wait for explicit approval before writing any code.

### 2. Plan First (plan.md)
- Before implementation, write a plan in `plan.md` for the user to review.
- Do not start coding until the user approves the plan.

### 3. Interview Before Planning (if needed)
- If clarification is needed before writing `plan.md`, conduct an interview first.
- Interview rules:
  - Ask deep, non-obvious questions (not surface-level ones).
  - Use multiple-choice format with 4-10 options per question.
  - State the total number of questions upfront at the beginning.
  - Mark recommended options and place the recommended choice as option 1.
  - Ask questions **one at a time**, waiting for the user's selection before proceeding.

### 4. Research Before Planning (if needed)
- If a `research.md` file exists, read and understand it thoroughly before writing `plan.md`.

### 5. Execution Order
```
Interview (if needed) -> research.md review (if exists) -> plan.md -> User approval -> Implementation
```
