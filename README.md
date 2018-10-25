# sass-colorsys

## Usage

### Import

```sass
@import "~sass-colorsys/sass-colorsys"
```

### Define your color set
```sass
$color-set: (
  (
    name: c1,
    color: #71cbc6,
    css_properties: (cl: color, bg: background, bdc: border-color, fl: fill),
    css_states: (ho: hover),
    darken: (d10: 10%),
    lighten: (l10: 10%),
    options: (normal:1)
  ),
  ...
);
```
### Make
```sass
@include make-color-styles($color-set);

```
