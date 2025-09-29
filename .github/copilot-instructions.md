# Copilot Instructions for Insight-Esportivo

## Project Overview
Insight-Esportivo is a Python-based sports analytics and insights platform. The project focuses on providing data-driven insights for sports enthusiasts, analysts, and professionals.

## Code Style and Standards

### Python Guidelines
- Follow PEP 8 style guidelines
- Use type hints for function parameters and return values
- Write comprehensive docstrings for all classes and functions
- Use meaningful variable and function names in English
- Prefer Portuguese for user-facing strings and comments when appropriate

### Project Structure
- Organize code into logical modules and packages
- Use `src/` directory for main application code
- Keep tests in `tests/` directory
- Configuration files should be in the root directory
- Documentation in `docs/` directory

### Dependencies and Environment
- Use `requirements.txt` for dependency management
- Consider using `pyproject.toml` for modern Python packaging
- Pin major versions for stability
- Use virtual environments for development

### Data Handling
- Handle sports data with appropriate data structures (pandas DataFrames recommended)
- Implement proper error handling for API calls and data processing
- Use appropriate data validation for sports metrics and statistics
- Follow data privacy best practices

### Testing
- Write unit tests for all business logic
- Use pytest as the testing framework
- Aim for high test coverage, especially for data processing functions
- Mock external API calls in tests

### Documentation
- Document all public APIs
- Include usage examples in docstrings
- Keep README.md updated with setup and usage instructions
- Document data sources and API endpoints used

### Security
- Never commit API keys or sensitive credentials
- Use environment variables for configuration
- Validate all external data inputs
- Follow security best practices for web scraping if applicable

## Specific to Sports Analytics
- Use consistent naming for sports entities (teams, players, matches)
- Implement proper data validation for sports statistics
- Handle different date/time formats for international sports data
- Consider timezone handling for global sports events
- Use appropriate statistical methods for sports analysis

## Git Workflow
- Use meaningful commit messages
- Create feature branches for new functionality
- Keep commits focused and atomic
- Include relevant tests with new features

## Performance Considerations
- Optimize data processing operations for large datasets
- Use efficient data structures for sports statistics
- Consider caching for frequently accessed data
- Profile code for performance bottlenecks in data analysis