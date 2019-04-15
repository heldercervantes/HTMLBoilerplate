# Helpers
A set of SCSS utils for multiple uses.

# unitless function
Given a value and a context to compare to, returns a unitless value.
Example: `line-height: unitless(20px, 16px);` Pass it a pixel-based font-size and line-height, returns `1.25`, which scales proportionally to whatever font-size is defined across breakpoints.

# em function
Same as unitless, but returns an EM value.

# expand list mixin
Expands a list based on property: value, such as a typography set.

# helper-center mixin
Uses the position:absolute + transform method for 2 axis centering.

# helper-center-vertical mixin
Uses the position:absolute + transform method for vertical centering.

# helper-clearfix mixin
Uses the pseudo-element approach to clearfix.