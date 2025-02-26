# Foundry VTT to Home Assistant Bridge

## Build Commands
- Build: `npm run build`
- Watch mode: `npm run watch`
- Lint: `npm run lint`
- Test all: `npm test`
- Test specific file: `npm test -- src/tests/services/home-assistant.service.test.ts`
- Test with pattern: `npm test -- -t "should publish data"`
- Test coverage: `npm run test:coverage`
- Clean build: `npm run clean`

## Code Style Guidelines
- **TypeScript**: Use strict mode with explicit typing, avoid `any` when possible
- **Naming**: camelCase for variables/methods, PascalCase for classes/interfaces
- **Imports**: Sort imports by type (core → external → internal)
- **Error Handling**: Use try/catch blocks for async operations with proper logging
- **Formatting**: 2-space indents, single quotes, semicolons required
- **Documentation**: JSDoc comments for public methods and classes
- **Testing**: Write unit tests for all service methods and core functionality
- **Architecture**: Follow the models/services pattern for code organization
- **Logging**: Use console.log with module ID prefix for consistent logging
- **Security**: Never expose or log Home Assistant tokens in plaintext