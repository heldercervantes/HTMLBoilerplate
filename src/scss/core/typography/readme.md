# Typography
Reusables, functions and mixins to manage everything related to fonts & typography.

## Fonts
Define your primary, secondary, more if needed in the `$fonts` list.

```
$fonts: (
  primary: (sans-serif),
  secondary: (Playfair Display, serif)
);
```

#### Using the font utils
```
@include useFont(secondary);
font-family: font(secondary);
```


## Sizes
Reusable size rules are stored in the `$sizes` list. Each size needs a mandatory `small` size which is used as a global value. In addition, it can have a `large` size that is tied to the layout-change breakpoint, or other values for specific breakpoints, always in a mobile-first approach.

```
$sizes: (
  base: (
    small: 12px,
    large: 14px
  ),
  large: (
    small: 16px,
    large: 18px,
    desktop: 20px
  )
);
```

#### Using the size utils
```
@include useSize(title) // Sets default and breakpoints sizes
font-size: size(title, large) // Returns a specific set+breakpoint value
```


## Weights
Define your default weights in a `$weights` list.

```
$weights: (
  regular: 400,
  medium: 600,
  bold: 700
);
```

#### Using the weight utils
```
@include useWeight(bold);
font-weight: weight(bold);
```


## Line heights
Define your default heights in a `$lineHeights` list.

These values are encouraged to be unitless, for consistency and so that they scale proportionally with whatever font-size is applied.

```
$lineHeights: (
  base: 1.25,
  tight: 0.9,
  wide: 1.5
);
```

#### Using the line-height utils
```
@include useLineHeight(bold);
line-height: lineHeight(bold);
```


## Letter spacings
Define your default spacings in a `$letterSpacings` list.

These values are encouraged to be EM, for consistency and so that they scale proportionally with whatever font-size is applied.

```
$letterSpacings: (
  base: 0,
  tight: -0.2em,
  wide: 0.2em
);
```

### Using the letter-spacing utils
```
@include useLetterSpacing(wide);
letter-spacing: letterSpacing(wide);
```


## Typography sets
Default, reusable typography sets are stored in a `$typeSets` list.

These sets should be independent of size. If i.e. `<h1>` and `<h2>` look the same but only differ in size, they should use the same typeset combined with different size rules.

Components that use very specific rules that are not going to be reused elsewhere are encouraged to avoid saturating this list.

```
$typeSets: (
  regular: (
    font-family: font(primary),
    weight: weight(regular),
    lineHeight: lineHeight(base)
  ),
  title: (
    font-family: font(secondary),
    font-weight: weight(bold),
    line-height: lineHeight(tight),
    letter-spacing: letterSpacing(wide),
    text-transform: uppercase,
    font-style: italic
  )
);
```

### Using the typeSet mixin
The `useType` mixin accepts a second optional parameter for specifying a size rule. This is only a shortcut that passes that second parameter to the `useSize` mixin.

``` 
@include useType(title);
@include useType(title, large);
```


