---
layout: post
title: Markup and Style Conventions
permalink: /markup-and-style/
categories: guidelines
nav: guidelines
max-width: md
status: draft
---

In the spirit of consistency and uniformity of both code and design, we make use of naming conventions in our markup and styles that allow us to keep maintainable, scalable, human-readable code.

# Follow the Weave Principles

1. Consistency
  - By imposing a naming convention, we have a basic structure to follow

2. Efficiency
  - While BEM can create some rather verbose class names, the efficiency comes in the form of instant understanding of how to apply conventions and how to interpret them.

3. Simplicity
  - Simple to understand: you should be able to read the class name and know what it does or affects.

4. Scalability
  - Scaling our code: class names do not conflict with each other and we will never find ourselves overwriting code or abusing `!important` in order to force the outcome we want.
  - Scaling our teams: those who are new to the Weave frontend should be able to pick up and understand how to apply it very quickly. A good naming convention is pivotal in making that happen.

5. Reality
  - We diverge from convention when it makes our lives easier. If it doesn't work for Stitch Fix, then it doesn't work--period.

# Namespacing

We made the decision to namespace our code using `.weave-`. While we begin to transition towards using the Weave design system, we need a way to avoid conflicts in the code and easily diagnose issues.

**Example:**

```css
.weave-grid-row {}
```

# BEM

[BEM](https://en.bem.info/) stands for **block**, **element**, **modifier**. For Weave, BEM is just a naming convention for CSS classes that allows us to keep our code modular. It's readable and descriptive. It's well-known and accepted as a practice.

(Some of this has been adapted from the [Kufak Code Style Guide](https://github.com/stitchfix/hellblazer/blob/master/code_style_guide.md))

1. Get to know the BEM syntax
  - [Guide to understanding the syntax](http://csswizardry.com/2013/01/mindbemding-getting-your-head-round-bem-syntax/)
	- **Example:**
```css
.block {}
.block__element {}
.block__element--modifier {}
```
```css
.media {}
.media__img {}
.media__img--reversed {}
```

1. Modular & reusable
  - Adding a component to a UI should feel the same in the design as it does in the code
  - Components are self-contained

2. Explicit CSS
  - Classes become human-readable so you can understand the output just by reading the markup
  - Specific purpose components
  - Low specificity classes (less `!important` throughout our code)

3. Decoupled style from structure **_when appropriate_**.
  - This idea doesn't always fit, but in the case of design systems, it's exactly what we want: mostly inflexible classes that create components, rather than fully-flexible microclasses
  - Flat CSS: our classes should usually live at the highest level and not be nested, which creates higher specificity and introduces confusion

# Conventions Beyond BEM

Ideally, we will have a code structure that matches our component designs in that every piece will be self-contained and standardized. In a more realistic world, we find value in stepping outside of the strict BEM best practices and make use of some of our own conventions, developed with our core values in mind.

## Utility Classes and Placeholders

**Example:**

```css
%u-clearfix,
.u-clearfix {
  &:before, &:after { content: " "; display: table; }
  &:after { clear: both; }
}
```

- Prefixed with `u-`
- Utility classes aid in common styling needs like positioning, structure, and spacing
- Should be single-purpose and `@extend`ed rather than marked up

## Javascript Classes

**Example**

`.js-click-target`

- Prefixed with `js-`
- Not for styling, only for javascript binding

## Component State Classes

**Example:**

```css
.weave-nav-link.has-dropdown {
  &::after {
    content: "▾";
  }
}
```

```css
.weave-nav-link.is-current {
  border-bottom: 3px solid color(mint-base);
}
```

- State classes indicate the state of a component and serve the purpose of specially styling states on a case-by-case basis. They should be treated similarly to the CSS states that already exist in the spec like `:hover` or `:focus`
- We break the convention of flat CSS so that states are tied directly to the component that they are affecting

# Writing Weave's CSS

- Stack class and placeholder names for shared styles

```css
.weave-h1,
.weave-h2,
.weave-h3 { }
```

- Leave a line-break between class declarations and between state classes

```css
.weave-h1 { }

.weave-button {

  &:hover { }

  &.is-loading { }
}
```

- Use `//` comment notation
- Err on the side of over-commenting in order to help the next developer
- Use 2 spaces indentation
- Use a space before the opening brace `{`
- Use a space after each colon `:`
- Closing brace `}` is on a new line
- Defer to [Harry Roberts's CSS Guidelines](http://cssguidelin.es/) otherwise
