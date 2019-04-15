# Breakpoints
Global breakpoints defined in the `$breakpoints` map. Mixins are made flexible, so that breakpoints can be configured just by editing this map.

The `layout-change` is mandatory and as the name implies, sets the threshold where the layout changes from small to large display mode. Breakpoint names are encouraged to be explanatory (tablet, tablet-horizontal, desktop, fhd...).

# Usage

```
    @include on(small) { ... } // Small screen mode
    @include on(large) { ... } // Large screen mode
    @include from(tablet-horizontal) { ... } // 1024px and up
    @include under(tablet-horizontal) { ... } // up to 1023px
    @include between(tablet, tablet-horizontal) { ... } // 768px to 1023px
```

Default values

```
$breakpoints: (
  tablet: 768px,
  tablet-horizontal: 1024px,
  desktop: 1200px,
  layout-change: 768px
);
```
