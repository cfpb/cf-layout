All notable changes to this project will be documented in this file.
We follow the [Semantic Versioning 2.0.0](http://semver.org/) format.

## 2.1.0 - 2015-12-03

## Added
- Added Featured Content Module pattern


## 2.0.0 - 2015-11-02
- Updated to use breakpoint variables in cf-core v1.2.0

This change _could_ break your existing projects if you have breakpoint values that do not match. Users should not attempt to automate the upgrade process due to the possibility of breaking the project layout. The best course of action is to:

1. Update the project to use cf-layout v2.0.0
2. Using Sublime Text or another editor with great search, CMD+Shift+F and search for `.respond-to`
3. Replace old variables or px values with the appropriate new variables

  Possible matches (test these yourself to be sure the change is what you expect):

  - `@mobile-max` or `.respond-to-max` with a value around 600px - `@bp-xs-max`
  - `@tablet-min` or `.respond-to-min` with a value around 600px - `@bp-sm-min`
  - `@tablet-max` or `.respond-to-max` with a value around 800px - `@bp-sm-max`
  - `@desktop-min` or `.respond-to-min` with a value around 800px - `@bp-med-min`
  - `@desktop-max` or `.respond-to-max` with a value around 1230px - `@bp-lg-max`
  - `@wall-min` or `.respond-to-min` with a value around 1230px - `@bp-xl-max`

  There's an additional breakpoint at 1020px that you may find useful (`@bp-med-max` and `@bp-lg-min`)


## 1.3.0 - 2015-10-19

### Added
- Added Hero pattern


## 1.2.0 - 2015-09-28
- Added `.block__flush` modifier for removing margin
  from all sides of a `.block`.
  Equivalent to
  `.block .block__flush-top .block__flush-bottom .block__flush-sides`.
- Changed bottom-padding of `.block__bg` to be double its current amount.
  Ems-equivalent of 30px on top and 60px on bottom.
- Added `.block__border-left`, `.block__border-right`, and `.block__border`
  modifiers to control all border settings.


## 1.1.2 - 2015-08-02

## Fixed

- typo in position declaration


## 1.1.1 - 2015-08-02

## Additions

- Added position: relative to content_wrapper only when necessary to avoid globally setting position on elements that don't need it.


## 1.1.0 - 2015-07-16

## Additions

- Added new `col-1-4` and `col-3-4` options

## Removals

- Extra mediaqueries
- Lots'o extra whitespace
- Lots'o mixed indentation

## Changes

- Updated the margin top to be mobile only to avoid resetting the property on larger displays
- Updated stacked columns margin top to not care what column size comes before it, as long as it's another column. This is far simpler than manually updating combinations, which is impossible to keep up with mixed grids.


## 1.0.1 - 2015-06-05

### Changed

- Moved @import rules to top of source file to make compilation cleaner.


## 1.0.0 - 2015-06-01

## Additions

- `@import` rules to pull in dependencies.

## Removals

- Grunt bower and concat tasks

## Changes

- `bowerrc` points to `src/vendor` (the now defunct Grunt task used to do this).
- Bumped to `1.0.0`.


## 0.3.0 - 2015-01-16

### Changed
- Replaces all CFPB color variables with non-CFPB colors. To add the CFPB theme
  to your project you will need to include the CFPB color palette and the
  Capital Framework theme overrides file. Both files can be found in the
  generator-cf repo here:
  <https://github.com/cfpb/generator-cf/tree/master/app/templates/src/static/css>
  Background info on the new Capital Framework color variables can be found at
  <https://github.com/cfpb/capital-framework/issues/115>.

### Updated
- NPM dependencies.


## 0.2.2 - 2015-01-06

### Fixed
- Updates `.stack-col` to use `display: block` on full-width columns. This puts it back into margin-collapsing
  mode. Without this, full-width inline-block columns will have double margins.


## 0.2.1 - 2014-12-29

### Fixed
- Left border width override for stacked columns.


## 0.2.0 - 2014-12-19

### Added
- `.content-l__full`, `.content-l__main`, and `.content-l__sidebar` modifier classes. These classes apply different breakpoints to their child `.content-l_col-RATIO` classes to suit the needs of varying-width containers.
- NOTE: the default breakpoint at which all the `.content-l_col-RATIO` classes display as columns is now 600px. This change affects .content-l_col-1-3, .content-l_col-2-3, .content-l_col-3-8, and .content-l_col-5-8, which previously became columns at 768px. To restore the previous behavior, add the `.content-l__full` modifier class to the parent `.content-l` element.
- `.stack-col`, `.stack-col-thirds`, and `.stack-col-eighths` mixin/helper classes to simplify changing `.content-l_col-RATIO` display from column to stacked.

### Removed
- `.content-l__stack-on-cols` modifier class -- use `.content-l__sidebar` instead.


## 0.1.1 - 2014-12-05

### Added
- Update cf-component-demo dev dependency to 0.9.0


## 0.1.0 - 2014-10-31

### Added
- Initial release.
