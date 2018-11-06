# sass-colorsys

## Usage

### Install package
npm i sass-colorsys

### Import in sass stylesheet

```sass
@import "~sass-colorsys/sass-colorsys"
```

### Define your sass color set
```sass
$color-variants: (
  lighten: (l10: 10%, l30: 30%),
  darken: (d10: 10%, d30: 30%)
);

$color-set: (
  (
    name: c1,
    color: #71cbc6,
    darken: map-get($color-variants, darken),
    lighten: map-get($color-variants, lighten),
    rule-types: (normal)
  ),
  ...
);
```
### build color styles
```sass
@include scs_build_colors($color-set);

```
