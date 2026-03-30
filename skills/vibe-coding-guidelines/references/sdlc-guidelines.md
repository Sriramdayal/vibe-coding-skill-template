# Python SDLC Guidelines

Follow these Software Development Life Cycle (SDLC) best practices when vibe-coding Python applications:

1. **Planning & Requirements Analysis**
   - Identify the scope, dependencies, and expected runtime environment (e.g., Python 3.10+, Docker).
   - Define technical requirements (e.g., libraries like `FastAPI`, `Pandas`, `SQLAlchemy`).

2. **Design & Setup**
   - Use a virtual environment (`venv`, `poetry`, or `uv`) to isolate project dependencies.
   - Define your data models using `pydantic` or standard `dataclasses`.
   - Structure code logically (e.g., separate routes, business logic, and data access layers).

3. **Implementation (Coding)**
   - Follow PEP 8 style guidelines.
   - Adhere strictly to the DSA principles outlined in `dsa-principles.md`.
   - Write modular, DRY (Don't Repeat Yourself) code. Prefer small, testable functions over monolithic scripts.
   - Use strict type hinting on all function signatures.

4. **Testing & QA**
   - Write unit tests using `pytest` for all core business logic before finalizing a feature.
   - Use `mock` (or `unittest.mock`) for external API calls and database connections during testing.
   - Run a static type checker like `mypy` and a linter/formatter like `ruff` or `flake8` + `black`.

5. **CI/CD & Deployment**
   - Automate testing and linting using GitHub Actions (in `.github/workflows`).
   - Use a `requirements.txt`, `Pipfile`, or `pyproject.toml` to lock dependencies for reproducible builds.
   - Containerize Python applications using Docker when deploying to production environments.

6. **Maintenance & Monitoring**
   - Implement robust centralized logging using Python's `logging` module or a structured logger like `loguru`. Avoid `print()` in production code.
   - Handle exceptions gracefully with specific `try...except` blocks rather than catching base `Exception`.
