# Release Notes

## Version 1.0.0

This release introduces a small Node.js app focused on safe startup behavior, predictable environment handling, and a minimal testable API.

### What's New

- Added a startup flow that loads environment variables with `dotenv`.
- Added a default runtime mode of `development` when `NODE_ENV` is not set.
- Added startup messages that clearly report the resolved runtime mode.
- Exposed reusable helpers for resolving the environment and generating startup output.

### Reliability and Safety

- Improved handling for missing environment configuration so the app can start predictably in local development.
- Kept sensitive environment files out of the public project configuration.

### Testing

- Added Node.js test coverage for default environment handling.
- Added test coverage for configured `NODE_ENV` values.
- Added test coverage for startup message generation.

### Getting Started

Install dependencies and start the app:

```bash
npm install
npm start
```

Run the test suite:

```bash
npm test
```

### Compatibility

- Requires Node.js with support for the built-in `node:test` runner.
- Uses `dotenv` for local environment configuration.
