# JavaScript Basics
- **Dynamic Typing**: Variables can hold any type (no static type enforcement).
- **Interpreted Language**: Executed line-by-line by JavaScript engine.
- **ECMAScript**: Official language specification (ES6/ES2015 major update).
- **Single Threaded**: Uses event loop for asynchronous operations.

# Variables & Scope
- **var**: Function-scoped, hoisted (avoid in modern JS).
- **let**: Block-scoped, mutable variable (preferred over var).
- **const**: Block-scoped, immutable binding (value can change for objects).
- **Hoisting**: Variable/function declarations moved to top of scope.
- **Temporal Dead Zone**: let/const inaccessible before declaration.

# Data Types
- **Primitives**: string, number, boolean, null, undefined, symbol, bigint.
- **Objects**: Collections of key-value pairs (including arrays, functions).
- **typeof**: Operator to check type (returns string).
- **Type Coercion**: Automatic type conversion (== vs ===).

# Functions
- **Function Declaration**: Hoisted (`function foo() {}`).
- **Function Expression`: Assigned to variable (`const foo = function() {}`).
- **Arrow Functions**: Shorthand, lexical `this` (`() => {}`).
- **IIFE**: Immediately Invoked Function Expression (`(function() {})()`).
- **Closures**: Functions remembering their lexical scope.

# Objects & Prototypes
- **Object Literal**: `{ key: value }` syntax.
- **Constructor**: `new` keyword creates object instances.
- **Prototype Chain**: Mechanism for inheritance (objects link to prototypes).
- **Class Syntax**: ES6 syntactic sugar over prototypes.
- **this Keyword**: Context-dependent (global/object/class/arrow functions).

# Arrays
- **Methods**: map, filter, reduce, forEach, find, some, every.
- **Spread Operator**: `[...arr]` for copying/merging.
- **Destructuring**: `const [a, b] = arr`.
- **Array-like Objects**: Arguments, NodeList (convert with `Array.from()`).

# Asynchronous JS
- **Callbacks**: Functions passed as arguments to async ops.
- **Promises**: Represent eventual completion (`then/catch/finally`).
- **async/await**: Syntactic sugar for promises (`try/catch` blocks).
- **Event Loop**: Mechanism handling call stack, callback queue, microtasks.
- **Microtasks**: Higher priority than regular callbacks (Promise reactions).

# ES6+ Features
- **Template Literals**: `` `Hello ${name}` `` with interpolation.
- **Destructuring**: Extract values from objects/arrays.
- **Default Parameters**: `function(a = 1) {}`.
- **Rest/Spread**: `...` operator for parameters/elements.
- **Modules**: `import/export` syntax.
- **Optional Chaining**: `?.` for safe property access.
- **Nullish Coalescing**: `??` for default values (null/undefined only).

# DOM Manipulation
- **querySelector**: Find single element (CSS selector syntax).
- **querySelectorAll**: Find all matching elements (static NodeList).
- **Event Listeners**: `element.addEventListener(event, handler)`.
- **Event Bubbling**: Events propagate up the DOM tree.
- **Event Delegation**: Listen on parent for dynamic children.

# Error Handling
- **try/catch/finally**: Handle synchronous errors.
- **Error Types**: SyntaxError, ReferenceError, TypeError, etc.
- **Custom Errors**: Extend Error class.
- **Promise Rejection**: Handle with `.catch()` or `try/catch` around await.

# Browser APIs
- **LocalStorage**: Persistent key-value storage (5MB limit).
- **SessionStorage**: Tab-specific storage (cleared on close).
- **Fetch API**: Modern replacement for XMLHttpRequest.
- **Web Workers**: Run scripts in background threads.
- **WebSocket**: Full-duplex client-server communication.

# Node.js Basics
- **CommonJS**: `require/module.exports` (vs ES modules).
- **Global Objects**: process, __dirname, __filename.
- **NPM**: Node package manager (largest JS ecosystem).
- **Event Emitter**: Publish-subscribe pattern core to Node.

# Best Practices
- **Strict Mode**: `'use strict'` catches common mistakes.
- **Immutable Patterns**: Avoid mutating objects/arrays directly.
- **Modular Code**: Small, single-purpose functions.
- **Linting**: ESLint for consistent style.
- **Type Checking**: TypeScript or JSDoc for large projects.

# Performance
- **Debouncing**: Group rapid-fire events (resize/scroll).
- **Throttling**: Limit function execution rate.
- **Memoization**: Cache function results.
- **Virtual DOM**: React's approach to efficient updates.

# Testing
- **Unit Tests**: Jest, Mocha (test individual functions).
- **Integration Tests**: Test component interactions.
- **E2E Tests**: Cypress, Playwright (full user flows).
- **Mocking**: Substitute real implementations for testing.

# Security
- **XSS Prevention**: Escape user input, use textContent over innerHTML.
- **CSRF Protection**: Anti-CSRF tokens for state-changing requests.
- **CORS**: Configure server-side for cross-origin requests.
- **Content Security Policy**: Restrict resource loading sources.
