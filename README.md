# styles
Bulma theme customizations for Sargassum apps

## Usage

This package merely provides a collection of SCSS files to include in a project; they must be preprocessed using your bundler into usable CSS. Support is provided for a dark theme SCSS file and a light theme. If you can include SCSS files from NPM package dependencies using `@import 'node_modules/package_name/path/to/file'`, then you can make a theme file with the following structure:

```
@charset 'utf-8';

// Shared base
@import 'node_modules/@sargassum-world/styles/global.scss';
@import 'node_modules/@sargassum-world/styles/typography.vars.scss';
@import 'node_modules/bulma/sass/utilities/mixins.sass';

// Application-specific parameters
// CUSTOMIZATION POINT: e.g. importing 'styles/app/fonts.scss' for a SCSS file of @font-face styles,
// or importing 'styles/app/layout.vars.scss' for a SCSS file of app-specific layout variables such
// as $gap, $navbar-height, etc.
// @import 'styles/app/fonts.scss';
// @import 'styles/app/layout.vars.scss';

// Shared
@import 'node_modules/@sargassum-world/styles/layout.scss';
@import 'node_modules/@sargassum-world/styles/colors-base.vars.scss';
@import 'node_modules/bulma/sass/utilities/initial-variables.sass';

// Theme colors
@import 'node_modules/@sargassum-world/styles/colors-light.vars.scss';

// Shared
@import 'node_modules/@sargassum-world/styles/theme.vars.scss';

// Bulma imports
@import 'node_modules/bulma/bulma.sass';

// Overrides & components
// CUSTOMIZATION POINT: e.g. importing 'styles/app/components/_all.scss' for styles of additional
// components
@import 'node_modules/@sargassum-world/styles/theme-overrides.scss';
@import 'node_modules/@sargassum-world/styles/components.scss';
// @import 'styles/app/components/_all.scss';
```

## License

Copyright Prakash Lab and the Sargassum project contributors.

SPDX-License-Identifier: Apache-2.0 OR BlueOak-1.0.0

You can use this project either under the [Apache 2.0 License](https://www.apache.org/licenses/LICENSE-2.0) or under the [Blue Oak Model License 1.0.0](https://blueoakcouncil.org/license/1.0.0); you get to decide. We chose the Apache license because it's OSI-approved, and because it goes well together with the [Solderpad Hardware License](http://solderpad.org/licenses/SHL-2.1/), which is a license for open hardware used in other related projects but not this project. We prefer the Blue Oak Model License because it's easier to read and understand.
