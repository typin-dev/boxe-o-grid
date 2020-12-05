# boxe-o-grid

Fluid and nestable flexbox based grid system.

Install using npm:
```
$ npm install --save boxe-o-grid
```

Import:
```scss
@import 'boxe-o-grid/_grid';
```


## Behaviour
- Columns are set to stack up to sass-mq `tablet` breakpoint.
- By default columns split width equaly.
- There is no limit on number of columns. 😱

## Example
```html
<div class="o-grid">
  <div class="o-grid__column">Column</div>
  <div class="o-grid__column">Column</div>
  <div class="o-grid__column">Column</div>
  <div class="o-grid__column">Column</div>
  <div class="o-grid__column">Column</div>
</div>
```

## Settings

### Column stack breakpoint
Customise the breakpoint until which columns stack. Handy when you got own breakpoints in sass-mq configuration.

Defaults:
```scss
// Stack breakpoints until defined breakpoint.
$boxe-column-stack-breakpoint: tablet !default;
```

Example:
```scss
$boxe-column-stack-breakpoint: desktop;
@import 'boxe-o-grid/_grid';
```

## Custom widths
Boxe grids work nicely with [boxe-u-widths](https://github.com/typin-dev/boxe-u-widths) utility classes.

Example:
```html
<div class="o-grid">
  <div class="o-grid__column">Column</div>
  <div class="o-grid__column">Column</div>
  <div class="o-grid__column">Column</div>
  <div class="o-grid__column u-2-5-tablet u-3-5-desktop">Column</div>
  <div class="o-grid__column">Column</div>
</div>
```

## Dependencies

[sass-mq](https://github.com/sass-mq/sass-mq) - Used for generating breakpoint based classes.
