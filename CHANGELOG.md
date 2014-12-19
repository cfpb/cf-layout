All notable changes to this project will be documented in this file.
We follow the [Semantic Versioning 2.0.0](http://semver.org/) format.


## 0.2.1 - 2014-12-05

### Added
- `.content-l__full`, `.content-l__main`, and `.content-l__sidebar` modifier classes. These classes apply different breakpoints to their child `.content-l_col-RATIO` classes to suit the needs of varying-width containers.
- NOTE: the default breakpoint at which all the `.content-l_col-RATIO` classes display as columns is now 600px. This change affects .content-l_col-1-3, .content-l_col-2-3, .content-l_col-3-8, and .content-l_col-5-8, which previously became columns at 768px. To restore the previous behavior, add the `.content-l__full` modifier class to the parent `.content-l` element.
- `.stack-col`, `.stack-col-thirds`, and `.stack-col-eighths` mixin/helper classes to simplify changing `.content-l_col-RATIO` display from column to stacked.

### Deprecated
- Nothing.

### Removed
- `.content-l__stack-on-cols` modifier class -- use `.content-l__sidebar` instead.

### Fixed
- Nothing.

## 0.1.1 - 2014-12-05

### Added
- Update cf-component-demo dev dependency to 0.9.0

### Deprecated
- Nothing.

### Removed
- Nothing.

### Fixed
- Nothing.

## 0.1.0 - 2014-10-31

### Added
- Initial release.

### Deprecated
- Nothing.

### Removed
- Nothing.

### Fixed
- Nothing.
