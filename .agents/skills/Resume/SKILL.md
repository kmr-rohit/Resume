```markdown
# Resume Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development patterns and conventions found in the "Resume" TypeScript repository. You'll learn how to structure files, write imports/exports, follow commit message patterns, and implement and test features in a consistent way. These patterns help maintain code clarity and project scalability, even without a formal framework.

## Coding Conventions

### File Naming
- Use **snake_case** for all file names.
  - Example: `user_profile.ts`, `resume_data.ts`

### Import Style
- Use **relative imports** to reference other modules.
  - Example:
    ```typescript
    import { getUserInfo } from './user_profile';
    ```

### Export Style
- Use **named exports** for all exported functions, types, or constants.
  - Example:
    ```typescript
    // In resume_data.ts
    export const resumeData = { ... };
    export function formatResume(data: Resume) { ... }
    ```

### Commit Patterns
- Commit messages are **freeform**, sometimes with prefixes.
- Average commit message length: ~40 characters.
  - Example:
    ```
    Add education section to resume data
    Fix typo in user_profile import
    ```

## Workflows

### Adding a New Feature
**Trigger:** When you need to add a new feature or section to the resume.
**Command:** `/add-feature`

1. Create a new file using snake_case (e.g., `work_experience.ts`).
2. Implement the feature using named exports.
3. Use relative imports to integrate with existing modules.
4. Write or update corresponding tests (`*.test.*` files).
5. Commit changes with a clear, concise message.

### Refactoring Code
**Trigger:** When improving code structure or readability.
**Command:** `/refactor`

1. Identify code to refactor (e.g., split large files, rename for clarity).
2. Rename files using snake_case if needed.
3. Update all relative imports accordingly.
4. Ensure all exports remain named.
5. Run tests to verify nothing is broken.
6. Commit with a descriptive message.

### Writing and Running Tests
**Trigger:** When adding or updating tests for your code.
**Command:** `/test`

1. Create or update test files using the `*.test.*` pattern (e.g., `resume_data.test.ts`).
2. Write tests using the project's preferred (unspecified) testing framework.
3. Run tests to ensure correctness.
4. Commit test changes with a clear message.

## Testing Patterns

- Test files follow the `*.test.*` naming convention.
  - Example: `resume_data.test.ts`
- The specific testing framework is **unknown**, but tests should be co-located with or near the modules they test.
- Tests should cover all exported functions and data structures.

## Commands
| Command        | Purpose                                      |
|----------------|----------------------------------------------|
| /add-feature   | Add a new feature or section to the resume   |
| /refactor      | Refactor code for clarity or structure       |
| /test          | Write and run tests for your code            |
```