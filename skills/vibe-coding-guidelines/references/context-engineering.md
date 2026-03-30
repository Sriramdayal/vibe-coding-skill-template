# Context Engineering for Python Vibe-Coding

Giving your AI agent the right context is the most impactful way to ensure high-quality Python code generation. Follow these practices to engineer your context effectively:

1. **Pin Relevant Files**
   - Explicitly include or address the exact files the agent needs. For a new API endpoint, include the `models.py` (database schema), `schemas.py` (Pydantic models), and `routes.py` (the target file).
   - Avoid dumping the entire repository context if only a few files are relevant.

2. **Provide Examples of "Good" Code**
   - If you want the agent to follow a specific internal pattern (e.g., a specific way you handle `SQLAlchemy` sessions or `FastAPI` dependencies), point it to an existing file that does it right: *“Use the same error-handling pattern found in `users/service.py`.”*

3. **Curate the Environment**
   - Use `.gitignore` and `.gitattributes` to keep auto-generated files, `__pycache__`, and virtual environments out of the agent's index.
   - Set up a strict `.cursorrules` or `.antigravity` file to globally enforce your Python style guide.

4. **Iterative Context Management**
   - Context windows have limits. If a conversation becomes too long and the agent starts forgetting constraints, summarize the progress, clear the history, and start a fresh session with only the most relevant revised context.
   - Clear context = Clear code.
