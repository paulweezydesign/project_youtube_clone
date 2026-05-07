```markdown
# project_youtube_clone Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill covers the core development patterns used in the `project_youtube_clone` repository, a TypeScript-based project that does not use a major framework. It details file naming conventions, import/export styles, commit message patterns, and testing approaches, providing clear examples and command suggestions to streamline development.

## Coding Conventions

### File Naming
- Use **PascalCase** for all file names.
  - **Example:**  
    ```
    VideoPlayer.ts
    UserProfile.ts
    ```

### Import Style
- Use **relative imports** for referencing other modules.
  - **Example:**
    ```typescript
    import { VideoList } from './VideoList';
    import { UserService } from '../services/UserService';
    ```

### Export Style
- Use **named exports** for all modules.
  - **Example:**
    ```typescript
    // In VideoPlayer.ts
    export function VideoPlayer() { ... }

    // In another file
    export const VIDEO_QUALITY_OPTIONS = [...];
    ```

### Commit Messages
- Freeform style, no enforced prefixes.
- Average commit message length: ~28 characters.
  - **Example:**  
    ```
    Add video search functionality
    Fix bug in comment section
    ```

## Workflows

### Adding a New Feature
**Trigger:** When implementing a new feature in the application  
**Command:** `/add-feature`

1. Create a new file using PascalCase for the feature.
2. Implement the feature using TypeScript.
3. Use relative imports to include any dependencies.
4. Export your feature using named exports.
5. Write corresponding tests in a `.test.ts` file.
6. Commit your changes with a clear, concise message.

### Fixing a Bug
**Trigger:** When resolving a bug in the codebase  
**Command:** `/fix-bug`

1. Locate the problematic code.
2. Apply the fix, maintaining code style conventions.
3. Update or add tests to cover the bug fix.
4. Commit with a descriptive message.

### Writing Tests
**Trigger:** When adding or updating tests  
**Command:** `/write-test`

1. Create or update a test file with the pattern `*.test.ts`.
2. Write tests for your feature or bug fix.
3. Run the tests using the project's test runner (framework unknown; refer to project docs or scripts).
4. Ensure all tests pass before committing.

## Testing Patterns

- Test files follow the `*.test.ts` naming convention.
- The testing framework is not specified; check project scripts or documentation for details.
- Place tests near the code they cover or in a dedicated `tests` directory.
- Example test file:
  ```typescript
  // VideoPlayer.test.ts
  import { VideoPlayer } from './VideoPlayer';

  describe('VideoPlayer', () => {
    it('should render without crashing', () => {
      // test implementation
    });
  });
  ```

## Commands
| Command       | Purpose                                  |
|---------------|------------------------------------------|
| /add-feature  | Scaffold and document a new feature      |
| /fix-bug      | Guide through fixing a bug               |
| /write-test   | Steps for adding or updating tests       |
```
