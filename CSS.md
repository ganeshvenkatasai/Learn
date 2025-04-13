# CSS3 Basics  
- **CSS (Cascading Style Sheets)**: Stylesheet language for describing HTML presentation.  
- **Inline CSS**: Applied directly via `style` attribute (highest specificity).  
- **Internal CSS**: Defined within `<style>` tags in HTML.  
- **External CSS**: Linked via `<link rel="stylesheet" href="file.css">`.  
- **CSS Syntax**: `selector { property: value; }`.  

# Selectors  
- **Element Selector**: `p { }` (selects all `<p>` elements).  
- **Class Selector**: `.class { }` (selects elements with `class="class"`).  
- **ID Selector**: `#id { }` (selects element with `id="id"`).  
- **Universal Selector**: `* { }` (selects all elements).  
- **Attribute Selector**: `[type="text"] { }` (selects by attribute).  
- **Descendant Selector**: `div p { }` (selects `<p>` inside `<div>`).  
- **Child Selector**: `div > p { }` (direct children only).  
- **Adjacent Sibling**: `h1 + p { }` (first `<p>` after `<h1>`).  
- **General Sibling**: `h1 ~ p { }` (all `<p>` after `<h1>`).  
- **Pseudo-class**: `a:hover { }` (state-based selection).  
- **Pseudo-element**: `p::first-line { }` (styles part of element).  

# Box Model  
- **Content**: Actual text/images in element.  
- **Padding**: Space between content and border.  
- **Border**: Edge around padding.  
- **Margin**: Space outside border (collapses between elements).  
- **box-sizing: border-box**: Includes padding/border in element's width/height.  

# Layout & Positioning  
- **display: block**: Takes full width (e.g., `<div>`).  
- **display: inline**: Flows in line (e.g., `<span>`).  
- **display: inline-block**: Inline but respects width/height.  
- **display: flex**: Enables Flexbox layout.  
- **display: grid**: Enables CSS Grid layout.  
- **position: static**: Default (follows document flow).  
- **position: relative**: Adjusts position relative to itself.  
- **position: absolute**: Positions relative to nearest positioned ancestor.  
- **position: fixed**: Stays fixed relative to viewport.  
- **position: sticky**: Toggles between relative/fixed based on scroll.  
- **z-index**: Controls stacking order of positioned elements.  

# Flexbox  
- **flex-direction**: `row` (default), `column`, `row-reverse`, `column-reverse`.  
- **justify-content**: Aligns items along main axis (`flex-start`, `center`, `space-between`).  
- **align-items**: Aligns items along cross axis (`stretch`, `center`, `baseline`).  
- **flex-wrap**: `wrap` allows items to wrap to new lines.  
- **flex-grow**: Expands item to fill available space.  
- **flex-shrink**: Allows item to shrink if needed.  
- **flex-basis**: Default size before remaining space is distributed.  
- **align-self**: Overrides `align-items` for individual items.  

# CSS Grid  
- **grid-template-columns/rows**: Defines column/row sizes.  
- **grid-gap**: Shorthand for `grid-row-gap` and `grid-column-gap`.  
- **grid-column/row**: Positions items in grid (`span` keyword for merging cells).  
- **grid-area**: Assigns item to named area or defines area.  
- **fr unit**: Fractional unit for flexible grid tracks.  

# Transitions & Animations  
- **transition**: `property duration timing-function delay`.  
- **transform**: `translate()`, `rotate()`, `scale()`, `skew()`.  
- **@keyframes**: Defines animation sequences.  
- **animation**: Shorthand for `name duration timing-function delay iteration-count direction`.  

# Responsive Design  
- **Media Queries**: `@media (max-width: 600px) { }` (condition-based styles).  
- **Viewport Meta Tag**: `<meta name="viewport" content="width=device-width, initial-scale=1">`.  
- **REM/EM Units**: Relative to root (`rem`) or parent (`em`) font size.  
- **VH/VW Units**: Viewport height (`vh`) and width (`vw`).  

# Advanced Features  
- **Variables (Custom Properties)**: `--main-color: #ff0000;` (use with `var(--main-color)`).  
- **Gradients**: `linear-gradient()` or `radial-gradient()`.  
- **Shadows**: `box-shadow` (box effect) and `text-shadow` (text effect).  
- **Filters**: `blur()`, `brightness()`, `contrast()` (applied to elements).  
- **Clip-path**: Creates clipping regions (e.g., circles, polygons).  

# Best Practices  
- **Mobile-First**: Design for small screens first, then scale up.  
- **BEM Naming**: Block__Element--Modifier (e.g., `.card__button--active`).  
- **Specificity**: Inline > ID > Class > Element (use wisely).  
- **Performance**: Minimize reflows/repaints, use `will-change` for optimizations.  
- **Accessibility**: High contrast, `prefers-reduced-motion`, semantic HTML.  
