# `/scss` User Documentation

This subdirectory is made to declutter one `.scss` file into smaller, cleaner files with meaningful structure.

## `/abstracts`

The **Abstracts** directory is reserved for Sass-exclusive utilities that can be used throughout other `.scss` files.

- **`_functions.scss`** - Used when creating function-style mixins that take one or more arguments
- **`_mixins.scss`** - Used for bundles of properties that do not take arguments like in _functions.scss
- **`_variables.scss`** - Used for defining variables that can be referenced throughout other files.
  - Uses `_functions.scss` to determine some variables

## `/base`

The **Base** directory is reserved to define font styles on this website, as well as any CSS resets to reduce style inconsistancies.

- **`_reset.scss`** - Used to define CSS resets in order to reduce style inconsistancies
- **`_typography.scss`** - Used to define typefaces, font styles, and other font-related properties

## `/components`

The **Components** directory is reserved for defining properties of single components, such as navbars, headers, footers, buttons, and more. Each component should have a separate stylesheet.

_These files will import other `.scss` files from preiously defined directories to create a consistent and cohesive style._

- **`_header.scss`** - Used for exclusive style definition, for the website's header

## `/pages`

The **Pages** directory is reserved for defining properties of individual pages on this website. Each page should have a separate stylesheet.

_These files will import other `.scss` files from preiously defined directories to create a consistent and cohesive style._

- **`_home.scss`** - Used for exclusive style definition, for the website's home page

## main.scss

The **main.scss** file is the main stylesheet that will be directly imported into the HTML using the `<link>` tag. This should import all items in the Pages directory, and anything else necessary, like `_reset.scss`.