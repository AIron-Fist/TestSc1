# Release Notes

## Version 1.0.0

Published: 2026-05-26
Target branch: `main`

This release introduces a small Node.js app focused on predictable startup behavior, safe local environment loading, and a minimal API that can be tested directly.

### What's New

- Added startup configuration through `dotenv`.
- Added a default runtime mode of `development` when `NODE_ENV` is not set.
- Added startup messages that report the resolved runtime mode.
- Exposed reusable helpers for resolving the environment and generating startup output.

### Reliability and Safety

- Improved behavior when local environment configuration is missing, so development startup remains predictable.
- Kept local environment files out of the public project configuration.
- Reduced startup behavior to small functions that are easier to test and reuse.

### Testing

- Added Node.js test coverage for default environment handling.
- Added test coverage for configured `NODE_ENV` values.
- Added test coverage for startup message generation.
- Verified with `npm test` on 2026-05-26: 3 tests passed.

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
