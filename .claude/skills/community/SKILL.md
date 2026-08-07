```markdown
# community Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill introduces the development patterns and workflows used in the `community` Python repository. You'll learn about the project's coding conventions, commit message style, testing approach, and the main workflow for updating documentation and integrations. This guide is ideal for contributors aiming to maintain consistency and efficiency in their contributions.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `integrationRegistry.py`, `userProfileHandler.py`

### Imports
- Use **relative imports** within the codebase.
  - Example:
    ```python
    from .utils import parseConfig
    from .models import Integration
    ```

### Exports
- Use **named exports** (explicitly export functions, classes, or variables).
  - Example:
    ```python
    __all__ = ["parseConfig", "Integration"]
    ```

### Commit Messages
- Follow **conventional commit** style.
- Common prefixes: `docs`, `docker`, `fix`
- Keep commit messages concise (average ~52 characters).
  - Example:
    ```
    docs: update integration instructions in README
    fix: correct typo in integrationRegistry.py
    docker: add support for arm64 architecture
    ```

## Workflows

### Update Documentation and Integrations
**Trigger:** When you need to document a new feature, connector, or clarify existing integration behavior.  
**Command:** `/update-docs-integration`

1. **Edit `README.md`**
   - Add or update documentation to describe new features, connectors, or clarify integration details.
   - Example:
     ```markdown
     ## New Integration: Slack
     This integration allows notifications to be sent to Slack channels.
     ```
2. **Update `integrations.json`**
   - Reflect the new or changed integration in the registry.
   - Example:
     ```json
     {
       "name": "slack",
       "description": "Slack channel notifications",
       "enabled": true
     }
     ```
3. **Commit your changes**
   - Use a conventional commit message, e.g.:
     ```
     docs: add Slack integration documentation
     ```
4. **Open a Pull Request**
   - Reference the changes and use the suggested command in the PR description if applicable.

## Testing Patterns

- **Test File Naming:** Test files follow the `*.test.*` pattern.
  - Example: `integrationRegistry.test.py`
- **Testing Framework:** Not explicitly detected; check existing test files for framework usage.
- **Test Example:**
  ```python
  def test_parseConfig():
      config = {"key": "value"}
      result = parseConfig(config)
      assert result["key"] == "value"
  ```

## Commands
| Command                  | Purpose                                                      |
|--------------------------|--------------------------------------------------------------|
| /update-docs-integration | Initiate the documentation and integrations update workflow. |
```
