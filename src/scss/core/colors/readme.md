# Colors
Global colors defined in the `$colors` map. Each color supports a `base` which is mandatory, and any number of variants for lighter, darker, etc.

## Usage

```
color: color(blue); // Returns base
color: color(blue, light); // Returns light variant
```

Sample values

```
$colors: (
  black: (
    base: #222222
  ),
  blue: (
    base: #3355AA,
    light: #99AAEE,
    dark: #222266
  ),
  red: (
    base: #990000
  )
);
```
