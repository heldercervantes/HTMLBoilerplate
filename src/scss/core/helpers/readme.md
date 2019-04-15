# Helpers
A set of SCSS utils for multiple uses.

## unitless function
`line-height: unitless(20px, 16px);`

Given a value and a context to compare to, returns a unitless value.
In this example we're passing a 20px line-height and 16px font size that we see in the design, which returns `1.25`. This value scales proportionally to whatever font-size is defined across breakpoints.

## em function
`line-height: em(20px, 16px);`

Same as unitless, but returns an EM value.

## expand list mixin
`@include expand(yourList);`

Expands a list based on property: value, such as a typography set.

## helper-center mixin
`@include helper-center;`

Uses the position:absolute + transform method for 2 axis centering.

## helper-center-vertical mixin
`@include helper-center-vertical;`

Uses the position:absolute + transform method for vertical centering.

## helper-clearfix mixin
`@include helper-clearfix;`

Uses the pseudo-element approach to clearfix.