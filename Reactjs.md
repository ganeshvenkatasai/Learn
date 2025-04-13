# React Fundamentals
- **Component-Based**: UI built from encapsulated, reusable components.
- **Declarative**: Describe what UI should look like (not how to update it).
- **Virtual DOM**: In-memory representation of actual DOM for efficient updates.
- **JSX**: Syntax extension combining HTML with JavaScript (not required but recommended).
- **Unidirectional Data Flow**: Parent-to-child props, events up via callbacks.

# Core Concepts
- **Components**: Functions or classes returning JSX (`function MyComponent() {}`).
- **Props**: Immutable data passed to components (`<Component prop="value" />`).
- **State**: Mutable data managed within components (`useState` hook).
- **Lifecycle Methods**: Class component hooks (mount/update/unmount).
- **Hooks**: Functions to "hook into" React features from function components.

# Key Hooks
- **useState**: Add state to function components (`const [state, setState] = useState(init)`).
- **useEffect**: Side effects in function components (`useEffect(() => {}, [deps])`).
- **useContext**: Access context values (`const value = useContext(MyContext)`).
- **useReducer**: State management for complex logic (`const [state, dispatch] = useReducer(reducer, init)`).
- **useRef**: Persistent mutable reference (`const ref = useRef(initialValue)`).
- **useMemo**: Memoize expensive calculations (`const memoized = useMemo(() => compute(), [deps])`).
- **useCallback**: Memoize functions (`const memoizedFn = useCallback(() => {}, [deps])`).

# Component Types
- **Function Components**: Modern preferred approach with hooks.
- **Class Components**: Legacy approach with lifecycle methods.
- **PureComponent**: Class component with shallow prop/state comparison.
- **memo**: Function component equivalent of PureComponent (`React.memo(MyComponent)`).

# State Management
- **Lifting State Up**: Share state by moving to common ancestor.
- **Context API**: Share data across component tree without prop drilling.
- **Redux**: Predictable state container for large apps (actions/reducers/store).
- **Recoil**: Experimental state management library by Facebook.
- **Zustand**: Lightweight state management alternative.

# Performance
- **Code Splitting**: Lazy-load components (`React.lazy(() => import())`).
- **Windowing**: Render only visible items (`react-window` library).
- **Profiler**: Identify performance bottlenecks (`<React.Profiler>`).
- **Optimizations**: Avoid reconciliation with keys, memoization.

# Routing
- **React Router**: Declarative routing (`<BrowserRouter>`, `<Route>`).
- **Dynamic Routing**: Load routes on demand (code splitting).
- **Navigation**: `<Link>` component or `useNavigate` hook.

# Styling
- **CSS Modules**: Scoped styles (`import styles from './module.css'`).
- **Styled Components**: CSS-in-JS library (`styled.div` syntax).
- **CSS-in-JS**: Emotion, styled-jsx alternatives.
- **Tailwind CSS**: Utility-first CSS framework.

# Advanced Patterns
- **Render Props**: Share code via prop that returns JSX.
- **Higher-Order Components**: Function that takes component, returns enhanced component.
- **Compound Components**: Components that work together (`<Select><Option/></Select>`).
- **Portals**: Render children outside DOM hierarchy (`createPortal`).
- **Error Boundaries**: Catch JavaScript errors in child components.

# Testing
- **Jest**: Test runner for unit tests.
- **React Testing Library**: Test components from user perspective.
- **Mocking**: Jest's mocking capabilities for dependencies.
- **Snapshot Testing**: Capture component output for regression testing.

# Best Practices
- **Single Responsibility**: Keep components small and focused.
- **Controlled Components**: Form elements managed by React state.
- **Key Prop**: Unique keys for list items (not array indexes).
- **Fragment**: Group elements without wrapper div (`<>...</>`).
- **Custom Hooks**: Extract reusable logic (`useSomething` convention).

# React Ecosystem
- **Next.js**: React framework for production (SSR, SSG).
- **Gatsby**: Static site generator for React.
- **Remix**: Full-stack React framework.
- **React Native**: Build mobile apps with React.

# Common Interview Topics
- **Virtual DOM vs Real DOM**: Diffing algorithm and reconciliation.
- **Hooks Rules**: Only call hooks at top level (no conditions/loops).
- **Component Lifecycle**: Mounting, updating, unmounting phases.
- **State vs Props**: When to use each.
- **Context vs Redux**: Tradeoffs for state management.
- **React Fiber**: New reconciliation engine (scheduling capabilities).
