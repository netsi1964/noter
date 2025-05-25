
```mdc
---
description: Guidelines for choosing clear, descriptive, and consistent names.
globs:
  - "**/*.js"
  - "**/*.ts"
  - "**/*.jsx"
  - "**/*.tsx"
  - "**/*.cs"
  - "**/*.py"
alwaysApply: false
---

- **Choose descriptive and unambiguous names** that clearly tell you what the variable, function, or class is for.
- The name should not require you to dig through the code to understand its purpose.
- Provide enough **context** if it helps clarify intent.
- Avoid **vague or overly broad names** like `data`.
- Avoid names that are **missing key information**, like a function named `process(input)` without specifying what is processed or how.
- The name should **match the actual meaning** in your domain or tech stack. Use terms correctly; for example, use "Generator" when creating something, not "Mapper".
- If you have similar things, give them **clear, specific names** to distinguish them.
- Keep your **method names uniform** and stick to **consistent patterns** (e.g., pick `get` or `fetch`, don't mix them). Consistency reduces mental overhead.
- Use **pronounceable names**.
- Use **searchable names**.
- A name should tell **why it exists, what it does, and how it is used**.

```

```mdc
---
description: Principles for writing small functions that do one thing (Single Responsibility).
globs:
  - "**/*.js"
  - "**/*.ts"
  - "**/*.jsx"
  - "**/*.tsx"
  - "**/*.cs"
  - "**/*.py"
alwaysApply: false
---

- Keep functions **small**.
- Functions should **only do one thing**. This follows the **Single Responsibility Principle (SRP)**.
- A function doing only one thing makes it more understandable, readable, maintainable, and easier to test.
- If a function becomes too long or complex, consider **breaking it into smaller, more manageable functions**.
- Use **descriptive names** for functions that clearly convey their purpose and behavior.

```

```mdc
---
description: Guidelines for function arguments and avoiding side effects.
globs:
  - "**/*.js"
  - "**/*.ts"
  - "**/*.jsx"
  - "**/*.tsx"
  - "**/*.cs"
  - "**/*.py"
alwaysApply: false
---

- Prefer **fewer arguments** for functions.
- Functions should **have no side effects**.
- **Don't use flag arguments**. Instead, split the method into several independent methods that can be called by the client without the flag.
- **Encapsulate nested conditionals** into separate functions with descriptive names to improve readability and clarity.

```

```mdc
---
description: Standards for writing effective and minimal comments.
globs:
  - "**/*.js"
  - "**/*.ts"
  - "**/*.jsx"
  - "**/*.tsx"
  - "**/*.cs"
  - "**/*.py"
alwaysApply: false
---

- Always try to **explain yourself in code** first. Code should be self-documenting through clear naming and structure.
- Use comments **sparingly**.
- Use comments as **explanation of intent** (the "why").
- Use comments as **clarification of code** when the code is complex.
- Use comments as **warning of consequences**.
- **Don't be redundant**; avoid commenting on obvious things.
- Don't add **obvious noise**.
- Don't use **closing brace comments**.
- **Don't comment out code**; just remove it.

```

```mdc
---
description: Principles for organizing code within files and classes.
globs:
  - "**/*.js"
  - "**/*.ts"
  - "**/*.jsx"
  - "**/*.tsx"
  - "**/*.cs"
  - "**/*.py"
alwaysApply: false
---

- Separate concepts **vertically**.
- Related code should appear **vertically dense**.
- Declare variables **close to their usage**.
- **Dependent functions** should be close to each other.
- **Similar functions** should be close to each other.
- Place functions in the **downward direction** (higher-level concepts/abstractions first, details later).
- Keep lines **short**.
- Don't use **horizontal alignment** (alignment).
- Use **white space** to associate related things and disassociate weakly related ones.
- Don't break **indentation**.
- Keep components **small and focused**, avoiding files larger than ~200 lines (e.g., in React/TypeScript). Break them into smaller subcomponents.

```

```mdc
---
description: Guideline to avoid needless repetition (DRY principle).
globs:
  - "**/*.js"
  - "**/*.ts"
  - "**/*.jsx"
  - "**/*.tsx"
  - "**/*.cs"
  - "**/*.py"
alwaysApply: false
---

- Follow the **DRY (Don't Repeat Yourself)** principle.
- **Duplication multiplies mistakes**. If logic exists in multiple places, changes risk inconsistency and bugs.
- **Consolidate logic**; when multiple places need the same logic, extract it once and reuse it using functions, classes, modules, or other abstractions.
- Reusing code makes it more efficient, consistent, and maintainable.
- Reduces the risk of errors and bugs as you only need to modify code in one place.

```

```mdc
---
description: Principles for keeping code simple and avoiding over-engineering.
globs:
  - "**/*.js"
  - "**/*.ts"
  - "**/*.jsx"
  - "**/*.tsx"
  - "**/*.cs"
  - "**/*.py"
alwaysApply: false
---

- Follow the **KISS (Keep It Simple, Stupid)** principle. Simpler is always better.
- **Reduce complexity** as much as possible. Complexity increases mental load.
- Ask yourself: Is there a simpler way? Could this function do less? Could this class have fewer responsibilities?
- Follow **YAGNI (You Aren't Gonna Need It)**. Build only what you need right now.
- **Avoid over-engineering** or coding for imaginary use cases that might never materialize. Premature architecture or optimization often adds unnecessary complexity.

```

```mdc
---
description: Rule for using named constants instead of magic numbers/strings.
globs:
  - "**/*.js"
  - "**/*.ts"
  - "**/*.jsx"
  - "**/*.tsx"
  - "**/*.cs"
  - "**/*.py"
alwaysApply: false
---

- **Replace magic numbers and strings with named constants**.
- Use constants with **meaningful names** that convey their purpose.
- This improves clarity and makes the code easier to understand.
- It makes code easier to modify, as changes only require modifying the constant declaration.
- Avoid encodings or appending prefixes/type information to names.

```

```mdc
---
description: Emphasis on maintaining consistency throughout the codebase.
globs:
  - "**/*.js"
  - "**/*.ts"
  - "**/*.jsx"
  - "**/*.tsx"
  - "**/*.cs"
  - "**/*.py"
alwaysApply: false
---

- **Be consistent**. If you do something a certain way, do all similar things in the same way.
- Consistency in naming, folder structure, API design, and coding patterns allows developers to navigate and extend codebases without constantly second-guessing themselves.
- Follow **standard conventions** for your programming language (e.g., PEP 8 for Python, camelCase/snake_case usage, indentation).
- Consider establishing and following **internal coding rules** or style guides for your organization.
- Take **inspiration from open-source projects** for effective conventions.

```

```mdc
---
description: General design principles from Clean Code.
globs:
  - "**/*.js"
  - "**/*.ts"
  - "**/*.jsx"
  - "**/*.tsx"
  - "**/*.cs"
  - "**/*.py"
alwaysApply: false
---

- Prefer **polymorphism** to if/else or switch/case statements.
- Use **dependency injection**.
- Follow the **Law of Demeter**: A class should know only its direct dependencies.
- Prefer **Composition over Inheritance**. Composition is more flexible and makes systems easier to extend and modify.
- **Hide internal structure** (Encapsulation).
- Prefer **dedicated value objects** to primitive types.
- The **base class should know nothing about its derivatives**.
- Prefer **non-static methods** to static methods.
- Objects/classes should be **small**, **do one thing**, and have a **small number of instance variables**.
- Avoid **logical dependency** (methods depending on something else in the same class to work correctly).

```

