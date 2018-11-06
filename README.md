# sass-colorsys

## Usage

### Install package
```
npm i sass-colorsys
```

### Import in sass stylesheet

```sass
@import "../node_modules/sass-colorsys/sass-colorsys.scss";
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
### Build color styles
```sass
@include scs_build_colors($color-set);

```

### Use declarative classes to apply colors
```html
<btn class="btn color-c1-bg color-c1-d10-bg-ho">test</btn>
```
Class syntax overview :

* __color-c1-bg__ : color c1 applied to background (bg)
* __color-c1-d10-bg-ho__ : color c1 variand darken 10% (d10) applied to background (bg) on hover (ho)

## More ?
Yes, It's a short overview ... I'm currently working on a more comprehensive documentation.