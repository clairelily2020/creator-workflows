---
name: long-term-plan
description: Help users create and manage long-term project plans by clarifying goals, milestones, tasks, dependencies, and schedule. Use for founder goals, content plans, learning plans, product launches, growth programs, or research projects.
---

# Long-Term Plan

Use this when the user needs to turn a large goal into a practical plan.

## Workflow

### 1. Clarify The Goal

Ask:

- What outcome should exist at the end?
- What is the time window?
- What is the starting point?
- What constraints matter?
- What would make the plan fail?

### 2. Define Milestones

Suggest 3 to 5 milestones.

Each milestone should have:

- clear output
- owner if known
- target date
- dependencies
- success signal

### 3. Break Milestones Into Tasks

For each milestone, create tasks with:

- action-oriented title
- expected output
- due date or sequence
- estimated effort
- dependency
- whether the user or agent can do it

### 4. Confirm The Plan

Show:

- milestone list
- task count
- critical path
- next three actions
- unresolved risks

## Output

```markdown
## Plan: {goal}

Time window:
{dates}

Outcome:
{end state}

Milestones:
1. {milestone} - output: {output} - due: {date}
2. ...

Tasks:
| Task | Output | Owner | Due | Depends on |
| --- | --- | --- | --- | --- |

Critical path:
{sequence}

Next three actions:
1. {action}
2. {action}
3. {action}

Risks:
- {risk}
```

## Rules

- Do not make a plan without a time window.
- Do not create vague tasks like "work on marketing."
- Keep the first week concrete.
- Surface dependencies instead of hiding them.
