# Contributing to Smart Grocery Restock Bot

Thank you for your interest in contributing to this project! This document provides guidelines and information for contributors.

## 🚀 Getting Started

### Prerequisites
- Python 3.9 or higher
- PostgreSQL installed locally
- Basic understanding of Telegram Bot API
- Familiarity with machine learning concepts (helpful but not required)

### Development Setup

1. **Fork and clone the repository**
   ```bash
   git clone https://github.com/yourusername/smart-grocery-restock-bot.git
   cd smart-grocery-restock-bot
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install development dependencies**
   ```bash
   pip install -r requirements-dev.txt
   ```

4. **Set up pre-commit hooks**
   ```bash
   pre-commit install
   ```

## 🎯 How to Contribute

### Reporting Issues
- Use the GitHub issue tracker
- Check if the issue already exists
- Provide detailed information:
  - Steps to reproduce
  - Expected vs actual behavior
  - Environment details (OS, Python version)
  - Logs/error messages

### Feature Requests
- Open an issue with the `enhancement` label
- Describe the feature and its use case
- Explain how it aligns with the project goals

### Code Contributions

#### Areas We Need Help With
- **ML Model Improvements**: Better prediction algorithms
- **Data Integration**: Additional data sources for context
- **User Experience**: Better notification timing and formatting
- **Testing**: Unit tests and integration tests
- **Documentation**: Code documentation and user guides
- **Performance**: Optimization and scalability improvements

#### Development Workflow

1. **Create a feature branch**
   ```bash
   git checkout -b feature/descriptive-name
   ```

2. **Make your changes**
   - Follow the coding standards (see below)
   - Add tests for new functionality
   - Update documentation if needed

3. **Test your changes**
   ```bash
   pytest tests/
   python -m flake8 src/
   python -m black src/ --check
   ```

4. **Commit your changes**
   ```bash
   git add .
   git commit -m "feat: add descriptive commit message"
   ```

5. **Push and create a Pull Request**
   ```bash
   git push origin feature/descriptive-name
   ```

## 📝 Coding Standards

### Python Style Guide
- Follow PEP 8
- Use `black` for code formatting
- Use `flake8` for linting
- Maximum line length: 88 characters (black's default)

### Code Structure
```
src/
├── bot/
│   ├── handlers/          # Telegram command handlers
│   ├── ml/               # Machine learning models
│   ├── data/             # Data processing and storage
│   └── utils/            # Utility functions
├── config/               # Configuration management
└── scripts/              # Database and setup scripts
```

### Commit Message Convention
We use conventional commits:
- `feat:` for new features
- `fix:` for bug fixes
- `docs:` for documentation changes
- `refactor:` for code refactoring
- `test:` for adding tests
- `chore:` for maintenance tasks

Example: `feat: add weather-based consumption prediction`

### Testing Guidelines
- Write unit tests for new functions
- Use pytest for testing framework
- Aim for >80% code coverage
- Test both success and failure cases
- Mock external API calls

### Documentation
- Use Google-style docstrings
- Update README.md for significant changes
- Add inline comments for complex logic
- Document API endpoints and data models

## 🔍 Code Review Process

All contributions go through code review:

1. **Automated Checks**: CI will run tests and linting
2. **Peer Review**: At least one maintainer will review your code
3. **Feedback**: Address any requested changes
4. **Merge**: Once approved, your PR will be merged

### Review Criteria
- Code quality and style compliance
- Test coverage and passing tests
- Documentation completeness
- Performance impact
- Security considerations

## 🧪 Testing

### Running Tests
```bash
# Run all tests
pytest

# Run with coverage
pytest --cov=src/

# Run specific test file
pytest tests/test_ml_models.py
```

### Test Structure
- Unit tests: `tests/unit/`
- Integration tests: `tests/integration/`
- Test data: `tests/fixtures/`

### Writing Tests
- Test file naming: `test_*.py`
- Test function naming: `test_function_name_scenario()`
- Use fixtures for common test data
- Mock external dependencies

## 🏷️ Labels and Issues

### Issue Labels
- `bug`: Something isn't working
- `enhancement`: New feature or improvement
- `documentation`: Documentation improvements
- `good first issue`: Good for newcomers
- `help wanted`: Extra attention needed
- `ml-model`: Machine learning related
- `telegram-api`: Telegram bot functionality

### Priority Labels
- `priority-high`: Critical issues
- `priority-medium`: Important improvements
- `priority-low`: Nice to have features

## 🤝 Community Guidelines

### Code of Conduct
- Be respectful and inclusive
- Focus on constructive feedback
- Help others learn and grow
- No harassment or discrimination

### Communication
- Use GitHub issues for bug reports and feature requests
- Join discussions in pull request comments
- Be patient with response times
- Ask questions if you're unsure

## 📚 Resources

### Documentation
- [Telegram Bot API](https://core.telegram.org/bots/api)
- [python-telegram-bot documentation](https://python-telegram-bot.readthedocs.io/)
- [Contextual Bandits](https://en.wikipedia.org/wiki/Multi-armed_bandit#Contextual_bandit)

### Development Tools
- [Black](https://black.readthedocs.io/) - Code formatting
- [Flake8](https://flake8.pycqa.org/) - Linting
- [Pytest](https://docs.pytest.org/) - Testing framework
- [Pre-commit](https://pre-commit.com/) - Git hooks

## 🎉 Recognition

Contributors will be:
- Listed in the project's contributors section
- Mentioned in release notes for significant contributions
- Invited to join the maintainer team for consistent contributors

Thank you for contributing to making grocery management smarter and more efficient! 🛒✨
