# Spacing
Set a default spacing unit and use multipliers to calculate spacing. Default unit is 4px. Also allows setting a list of default spacing values that can be reused.

The same `spacing(...)` function accepts either a number which is interpreted as a multiplier, or a string which it looks for in the default spacings list.

# Usage

```
padding: 0 spacing(5); // 20px
padding: 0 spacing(wide): // 40px
```

Sample values

```
$spacing-unit: 4px;

$spacings: (
  base: 5,
  wide: 10,
  xwide: 25
);
```
