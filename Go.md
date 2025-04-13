# Go Basics
- **Static Typing**: Variables have explicit types checked at compile-time.
- **Compiled Language**: Code compiles directly to machine code (no VM).
- **Garbage Collected**: Automatic memory management.
- **Cross-Platform**: Supports Windows, Linux, macOS, etc.
- **Single Binary**: Compiles to self-contained executable.

# Language Structure
- **Packages**: Code organization unit (every file belongs to a package).
- **main()**: Entry point of executable programs.
- **Imports**: Access external packages using `import`.
- **Visibility**: Uppercase = exported (public), lowercase = unexported (private).

# Variables & Constants
- **var**: Declares variables (`var x int = 10`).
- **:=**: Short declaration (`x := 10` infers type).
- **const**: Unchanging values (`const pi = 3.14`).
- **Zero Values**: Default values (0, "", false, nil).

# Data Types
- **Basic Types**: int, float64, bool, string.
- **Composite Types**: array, slice, map, struct.
- **Reference Types**: slice, map, channel, pointer, function.
- **Type Conversion**: Explicit (`float64(42)`).

# Functions
- **Multiple Returns**: Functions can return multiple values.
- **Named Returns**: Return variables can be named in signature.
- **Variadic Functions**: Accept variable arguments (`...T`).
- **Defer**: Schedule function call to run after return.
- **Anonymous Functions**: Functions without names (closures).

# Control Structures
- **if-else**: No parentheses required around condition.
- **switch**: No need for `break` statements.
- **for**: Only looping construct (`for i:=0; i<10; i++`).
- **range**: Iterate over slices, maps, channels.

# Pointers
- **&**: Address-of operator (`&x`).
- **\***: Dereference operator (`*ptr`).
- **No Pointer Arithmetic**: Unlike C/C++.

# Structs
- **Custom Types**: `type Person struct { name string }`.
- **Methods**: Functions with receiver (`func (p Person) greet() {}`).
- **Embedding**: Composition over inheritance.

# Interfaces
- **Implicit Implementation**: Types implement interfaces by method matching.
- **Empty Interface**: `interface{}` accepts any type (like `Object` in Java).
- **Type Assertion**: Extract concrete value (`val.(int)`).

# Concurrency
- **goroutine**: Lightweight thread (`go func()`).
- **channel**: Communication between goroutines (`make(chan int)`).
- **select**: Wait on multiple channel operations.
- **sync Package**: Mutexes, WaitGroups for synchronization.

# Error Handling
- **error Type**: Built-in interface for errors.
- **Multiple Returns**: Typically `(result, error)` pattern.
- **panic/recover**: For exceptional errors (rarely used).

# Packages & Modules
- **go.mod**: Module definition file.
- **go.sum**: Dependency checksums.
- **go get**: Add dependencies.
- **init()**: Special package initialization function.

# Testing
- **\*_test.go**: Test files.
- **testing Package**: Built-in testing support.
- **Table Tests**: Parameterized tests using struct slices.
- **Benchmarks**: Performance testing (`BenchmarkXxx` functions).

# Best Practices
- **gofmt**: Enforce standard formatting.
- **Effective Go**: Official style guide.
- **Short Names**: Prefer `i` over `index` for locals.
- **Error Handling**: Always check errors.
- **Documentation**: Comments before declarations (`godoc` format).

# Common Packages
- **fmt**: Formatted I/O.
- **os**: Operating system interaction.
- **io/ioutil**: File operations.
- **net/http**: HTTP client/server.
- **encoding/json**: JSON handling.
- **time**: Date/time operations.
- **sync**: Concurrency primitives.

# Memory Management
- **Stack vs Heap**: Compiler decides allocation location.
- **Escape Analysis**: Determines if variable escapes function scope.
- **GC Tuning**: GOGC environment variable controls GC aggressiveness.

# Advanced Topics
- **Reflection**: runtime type inspection (`reflect` package).
- **cgo**: Call C code from Go.
- **Assembly**: Go supports plan9 assembly.
- **Context**: Propagation of deadlines/cancellation signals.
- **Generics**: Type parameters (Go 1.18+).
