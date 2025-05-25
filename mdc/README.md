# MDC Rules Directory

This directory contains `.mdc` rule files that define coding guidelines and best practices for your project. These rules can be used by AI tools (such as Cursor or other code assistants) to provide consistent, high-quality code suggestions and reviews based on your team's standards.

## How to Use the `.mdc` Files

1. **Location**: Place your `.mdc` files in the `.cursor/rules` directory in your project root (or another directory recognized by your tool).
2. **Activation**: Your AI/code assistant will automatically detect and apply these rules to files matching the `globs` patterns defined in each `.mdc` file.
3. **Customization**: You can edit, add, or remove `.mdc` files to tailor the rules to your project's needs. Adjust the `globs` patterns to target specific file types or folders.
4. **Best Practice**: Keep your rules modular—one principle or topic per file—for clarity and maintainability.

## Existing Rule Files

Below is a summary of the current `.mdc` files and their purposes:

- [**01_naming_conventions.mdc**](01_naming_conventions.mdc): Guidelines for choosing clear, descriptive, and consistent names for variables, functions, and classes.
- [**02_single_responsibility.mdc**](02_single_responsibility.mdc): Principles for writing small functions that do one thing (Single Responsibility Principle).
- [**03_function_arguments.mdc**](03_function_arguments.mdc): Guidelines for minimizing function arguments and avoiding side effects.
- [**04_comments.mdc**](04_comments.mdc): Standards for writing effective and minimal comments.
- [**05_code_organization.mdc**](05_code_organization.mdc): Principles for organizing code within files and classes for readability and maintainability.
- [**06_dry_principle.mdc**](06_dry_principle.mdc): Guidelines to avoid needless repetition (DRY principle).
- [**07_kiss_yagni.mdc**](07_kiss_yagni.mdc): Principles for keeping code simple (KISS) and avoiding over-engineering (YAGNI).
- [**08_constants.mdc**](08_constants.mdc): Rule for using named constants instead of magic numbers or strings.
- [**09_consistency.mdc**](09_consistency.mdc): Emphasis on maintaining consistency throughout the codebase.
- [**10_clean_code_design.mdc**](10_clean_code_design.mdc): General design principles inspired by Clean Code, including encapsulation, composition, and dependency management.
- [**mcp_context7_usage.mdc**](mcp_context7_usage.mdc): Guidelines for using Context7-compatible libraries and integrations in your project.
- [**mcp_git_usage.mdc**](mcp_git_usage.mdc): Guidelines for using Git MCP servers and automating repository tasks.
- [**mcp_server_usage.mdc**](mcp_server_usage.mdc): Guidelines for secure and effective use of MCP servers in your project.
- [**mcp_task_management.mdc**](mcp_task_management.mdc): Guidelines for managing tasks and workflows with MCP Task Master.

## Extending the Rules

To add new rules, simply create a new `.mdc` file in the `.cursor/rules` directory. Use the same format as the existing files:

```
---
description: Short summary of the rule.
globs:
  - "**/*.js"
  - "**/*.ts"
  # ...
alwaysApply: false
---

- List your guidelines here.
```

Keep your rules clear and focused. For more information, refer to your code assistant's documentation.