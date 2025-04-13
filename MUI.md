# MUI Fundamentals
- **Material-UI**: React UI library implementing Google's Material Design.
- **Component-Based**: Pre-built, customizable React components.
- **CSS-in-JS**: Styled with emotion/styled-components (v5+).
- **Theming**: Centralized design system management.
- **Accessibility**: WCAG-compliant components out-of-the-box.

# Core Concepts
- **ThemeProvider**: Context for theme distribution.
- **sx prop**: Shortcut for inline styling with theme access.
- **Styled API**: CSS utility for component styling.
- **Box Component**: CSS utility component (like div with sx support).
- **Container**: Responsive layout container.

# Layout Components
- **Grid**: Flexbox-based responsive grid (items + containers).
- **Stack**: 1D layout component (replaces Grid for simple cases).
- **AppBar**: Top application bar.
- **Drawer**: Side navigation panel.
- **Paper**: Elevated surface with shadow.

# Input Components
- **Button**: Contained/outlined/text variants with icons.
- **TextField**: Form inputs with labels/validation.
- **Select**: Dropdown selector.
- **Checkbox**: Toggle selection.
- **Radio**: Single selection from options.
- **Switch**: Toggle switch.
- **Slider**: Range selection.
- **Autocomplete**: Combobox with suggestions.

# Data Display
- **Typography**: Consistent text styling.
- **Avatar**: User/profile images.
- **Chip**: Compact element for input/attribute.
- **Badge**: Small status badge on elements.
- **List**: Vertical list of items.
- **Table**: Data table with sorting/pagination.
- **Card**: Content container with header/media/actions.

# Feedback Components
- **Alert**: Feedback messages (success/error/warning/info).
- **Snackbar**: Temporary notification popup.
- **Dialog**: Modal popup window.
- **Backdrop**: Screen dimmer for attention focus.
- **Progress**: Linear/circular loading indicators.
- **Skeleton**: Content placeholder during loading.

# Navigation
- **BottomNavigation**: Mobile-style bottom nav bar.
- **Breadcrumbs**: Secondary navigation hierarchy.
- **Tabs**: Horizontal tab navigation.
- **Stepper**: Multi-step progress indicator.

# Theming System
- **createTheme**: Generate custom theme object.
- **Palette**: Color system configuration.
- **Typography**: Font hierarchy settings.
- **Spacing**: 8px-based default spacing scale.
- **Breakpoints**: Responsive design thresholds.
- **Z-index**: Layer management system.

# Advanced Features
- **CSS Variables**: Dynamic theming (v5.1+).
- **Styled Engine**: Zero-runtime CSS-in-JS (v5+).
- **Unstyled Components**: Base components without styles.
- **System Props**: Style shorthand props (mt=2 for margin-top).
- **Joy UI**: Newer aesthetic alternative (v5+).

# Utility Hooks
- **useTheme**: Access theme in components.
- **useMediaQuery**: Responsive layout hooks.
- **useScrollTrigger**: Scroll position detection.
- **useAutocomplete**: Autocomplete logic hook.

# Best Practices
- **Theme Customization**: Override defaults at theme level.
- **Responsive Design**: Use breakpoints with sx prop.
- **Component Composition**: Build complex UIs from simple components.
- **Performance**: Memoize styled components.
- **Accessibility**: Use proper ARIA labels.

# Common Patterns
- **Dark Mode**: Theme switching with localStorage.
- **Form Validation**: Combine with Formik/react-hook-form.
- **Data Grid**: Use for complex tables (requires license).
- **Internationalization**: Integrate with react-i18next.

# Integration
- **Next.js**: Works seamlessly with App Router.
- **React Router**: Navigation integration.
- **Redux**: State management pairing.
- **Storybook**: Component documentation.

# Troubleshooting
- **CSS Specificity**: Use styled() API for override control.
- **Server-Side Rendering**: Ensure class name matching.
- **Bundle Size**: Use path imports (@mui/material/Button).
- **Legacy Styles**: Migrate JSS to emotion (v4 → v5).
