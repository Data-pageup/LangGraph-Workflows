# LangGraph Workflows

This repository demonstrates core LangGraph concepts through different LLM workflows, including state management, prompt chaining, iterative workflows, persistence, human-in-the-loop interactions, and subgraphs.
## Topics Covered

### 1. Temperature Conversion Workflow
**File:** `1_Temperature_Conversion_Workflow.ipynb`

A basic LangGraph workflow that performs temperature conversion.

Concepts covered:
- StateGraph
- Nodes
- Edges
- START and END nodes
- Passing state between nodes

---

### 2. Simple Q&A LLM Workflow
**File:** `2_Simple_QA_LLM_Workflow.ipynb`

A simple question-answering workflow using an LLM.

Concepts covered:
- LLM integration
- State management
- Calling an LLM inside a LangGraph node
- Returning updated state

---

### 3. Prompt Chaining Workflow
**File:** `3_Prompt_Chaining_Workflow.ipynb`

Multiple LLM steps are connected sequentially where the output of one step becomes the input for the next.

Concepts covered:
- Prompt chaining
- Sequential workflows
- Passing outputs between nodes
- Multi-step LLM processing

---

### 4. Employee Analytics Workflow
**File:** `4_Employee_analytics_Workflow.ipynb`

A workflow designed to process and analyze employee-related information.

Concepts covered:
- Structured state
- Multi-node workflows
- Data processing using LangGraph

---

### 5. Essay Workflow
**File:** `5_Essay_workflow.ipynb`

A workflow for generating and processing essays using multiple steps.

Concepts covered:
- Content generation
- Sequential LLM workflows
- Passing generated content between nodes

---

### 6. Content Moderation Workflow
**File:** `6_Content_Moderation_Workflow.ipynb`

A workflow that checks and processes content based on moderation logic.

Concepts covered:
- Conditional processing
- LLM-based decision making
- Content validation workflows

---

### 7. Review Workflow
**File:** `7_Review_workflow.ipynb`

A workflow where generated content is reviewed and processed.

Concepts covered:
- Generation and review pipelines
- Multi-step workflows
- Feedback-based processing

---

### 8. Iterative Workflows
**File:** `8_Iterative_Workflows.ipynb`

Workflows that repeatedly execute nodes until a particular condition is met.

Concepts covered:
- Loops in LangGraph
- Conditional edges
- Iterative processing
- State updates across iterations

---

### 9. Persistence
**File:** `9_Persistence.ipynb`

Exploring how LangGraph saves and restores workflow state.

Concepts covered:
- Checkpointers
- `MemorySaver` / `InMemorySaver`
- Persistent state
- Thread IDs
- Conversation/session memory

---

### 10. Human-in-the-Loop (HITL)
**File:** `10_HITL.ipynb`

A workflow where execution pauses and waits for human approval before continuing.

Concepts covered:
- `interrupt()`
- Human approval
- Pausing graph execution
- Resuming execution using `Command(resume=...)`
- Checkpointers
- Thread IDs

Example flow:

```text
User Input
    ↓
Graph Execution
    ↓
Interrupt
    ↓
Human Approval / Rejection
    ↓
Resume Graph
    ↓
Final Output
