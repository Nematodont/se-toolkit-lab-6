Call an LLM from Code
Build a CLI that connects to an LLM and answers questions. This is the foundation for the agent you will build in the next tasks.

What you will build
A Python CLI program (agent.py) that takes a question, sends it to an LLM, and returns a structured JSON answer. No tools or agentic loop yet — just the basic plumbing: parse input, call the LLM, format output. You will add tools and the agentic loop in Tasks 2–3.

User question → agent.py → LLM API → JSON answer
Input — a question as the first command-line argument:

uv run agent.py "What does REST stand for?"
Output — a single JSON line to stdout:

{"answer": "Representational State Transfer.", "tool_calls": []}
Rules:

answer and tool_calls fields are required in the output.
tool_calls is an empty array for this task (you will populate it in Task 2).
Only valid JSON goes to stdout. All debug/progress output goes to stderr.
The agent must respond within 60 seconds.
Exit code 0 on success.
