<general_rules>
- Linting & Formatting: The repository uses `prettier` for formatting and `eslint` for linting. Commands are available in `package.json` to run these checks and fixes across the monorepo using `turbo` (e.g., `yarn format`, `yarn lint`, `yarn lint:fix`). A pre-commit hook (`lint-staged`) is also configured to format and lint staged files.
- API Consistency: A key guideline from `CONTRIBUTING.md` is to maintain API consistency with the Python version of LangChain. Any new abstractions should be proposed and discussed in an issue before implementation.
- Documentation: All new classes and methods should be well-documented using TSDoc, as the API documentation is auto-generated.
</general_rules>
<repository_structure>
- Monorepo: The project is a monorepo managed with Yarn workspaces and Turbo.
- Workspaces: The main workspaces defined in `package.json` are `langchain`, `langchain-core`, `libs/*`, `examples`, and `docs/*`.
- Core Modules: The `README.md` file outlines the core conceptual modules of the library: "Model I/O", "Retrieval", and "Agents".
- Examples: New examples should be added to the `examples/src` directory.
</repository_structure>
<dependencies_and_installation>
- Package Manager: The repository uses `yarn@3.4.1`.
- Node Version: The required Node.js version is `>=18`.
- Installation: To install all dependencies for all workspaces, one should run `yarn` in the root directory.
<testing_instructions>
- Unit Tests: Unit tests can be run with `yarn test:unit`.
- Integration Tests: Integration tests require Docker and can be run with `yarn test:int`. This command handles starting and stopping the required Docker containers.
- Environment Tests: There are specific tests to ensure compatibility across different JavaScript environments (Node.js ESM/CJS, Edge, Browser). These tests also use Docker and can be run with `yarn test:exports:docker`.
- Main Test Command: The `yarn test` command runs a sequence of unit tests, builds, and environment tests.
<pull_request_formatting>
- Template: The repository provides a pull request template in `.github/pull_request_template.md`.
- Content: The template requires a description of the changes, a reference to the issue being fixed (if any), and relevant context. It also includes an optional field for a Twitter handle for contributor shoutouts.
</pull_request_formatting>

