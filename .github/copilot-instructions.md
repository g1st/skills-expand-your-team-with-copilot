### Copilot Instructions

## Project Overview

This is a Python FastAPI application for Mergington High School's extracurricular activities management system. The application allows students to view and sign up for school activities.

## Development Setup

### Prerequisites
- Python 3.x
- pip (Python package manager)

### Installation
```bash
pip install -r src/requirements.txt
```

### Running the Application
```bash
python -m uvicorn src.app:app --host 0.0.0.0 --port 8000
```

Access the application:
- Frontend: http://localhost:8000
- API Documentation: http://localhost:8000/docs
- Alternative Docs: http://localhost:8000/redoc

### Debugging
Use VS Code's "Launch Mergington WebApp" configuration (F5) for debugging with auto-reload enabled.

## Project Structure

```
src/
├── app.py              # Main FastAPI application entry point
├── backend/
│   ├── database.py     # In-memory database with sample data
│   └── routers/        # API route handlers
│       ├── activities.py
│       └── auth.py
├── static/             # Frontend HTML/CSS/JS files
└── requirements.txt    # Python dependencies
```

## Coding Guidelines

### Technology Stack
- **Backend**: Python with FastAPI framework
- **Frontend**: HTML, CSS, JavaScript (no frameworks)
- **Database**: In-memory (data resets on server restart)
- **Allowed Languages**: Python, HTML, CSS, JavaScript only

### Code Quality
- Write simple, maintainable code suitable for non-technical staff
- Avoid software jargon in comments and documentation
- Use clear directory structure (no single large files)
- Add unit tests for any code handling grades, scores, or numerical data
- Keep functions small and focused

### Security & Privacy
- Never hardcode secrets, passwords, or sensitive information
- Implement proper authentication for sensitive operations
- Use secure password hashing (argon2 is already configured)
- Handle personal information with care

### Documentation
- Update README.md for user-facing features
- Use docs/ directory for detailed documentation
- Explain features in simple, non-technical terms
- Assume users will need to reference documentation frequently

## Testing

Currently, there is no test suite. When adding tests:
- Use pytest as the testing framework
- Focus on critical business logic (especially numerical calculations)
- Add tests in a `tests/` directory
- Name test files as `test_*.py`

## Common Commands

| Command | Purpose |
|---------|---------|
| `pip install -r src/requirements.txt` | Install dependencies |
| `python -m uvicorn src.app:app --reload` | Run with auto-reload |
| `python -m uvicorn src.app:app --host 0.0.0.0 --port 8000` | Run production mode |

## Additional Context

For detailed school-specific context, architecture decisions, and user interaction guidelines, see [copilot-instructions-ext.md](copilot-instructions-ext.md).
