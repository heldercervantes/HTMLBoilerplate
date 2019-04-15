# Breakpoints
Global breakpoints defined in the `$breakpoints` map. Mixins are made flexible, so that breakpoints can be configured just by editing this map.

The `layout-change` is mandatory and as the name implies, sets the threshold where the layout changes from small to large display mode. Breakpoint names are encouraged to be explanatory (tablet, tablet-horizontal, desktop, fhd...).

## Usage
The most basic use is the `on` mixin. This only accepts `small` or `large` as a parameter.

Then there are mixins for targetting the other breakpoints. These are `from`, `under` and `between`.

`from` lets you specify a breakpoint where you want to start from, going up. `from(tablet)` specifies tablet and up.

`under` specifies viewports until the provided breakpoint, not including. `until(tablet)` means every size up to, but not including tablet.

`between` requires two parameters and is a combination of the previous two mixins. `between(tablet, tablet-horizontal)` targets sizes of 768 to 1023px.

```
@include on(small) { ... } // Small screen mode
@include on(large) { ... } // Large screen mode
@include from(tablet-horizontal) { ... } // 1024px and up
@include under(tablet-horizontal) { ... } // up to 1023px
@include between(tablet, tablet-horizontal) { ... } // 768px to 1023px
```

Sample values

```
$breakpoints: (
  tablet: 768px,
  tablet-horizontal: 1024px,
  desktop: 1200px,
  layout-change: 768px
);
```
