<!-- @file Instructions for subtheming using the SASS Starterkit. -->
# SASS Starterkit

Below are instructions on how to create a Bootstrap sub-theme using a SASS
preprocessor.

- [Prerequisites](#prerequisites)
- [Additional Setup](#setup)
- [Override Styles](#styles)
- [Override Settings](#settings)
- [Override Templates and Theme Functions](#registry)

## Prerequisites

@TODO

## Additional Setup {#setup}
Download and extract the **latest** [Bootstrap Framework Source Files] into your
new sub-theme. After it has been extracted, the folder should read `./subtheme/bootstrap`.

If for whatever reason you have an additional `bootstrap` folder wrapping the
first `bootstrap` folder (e.g. `./subtheme/bootstrap/bootstrap`), remove the
wrapping `bootstrap` folder. You will only ever need to touch these files if
or when you upgrade your version of the [Bootstrap Framework].

{.alert.alert-warning} **WARNING:** Do not modify the files inside of
`./subtheme/bootstrap` directly. Doing so may cause issues when upgrading the
[Bootstrap Framework] in the future.

## Override Styles {#styles}
The `./subtheme/ssass/variable-overrides.scss` file is generally where you will
the majority of your time overriding the variables provided by the [Bootstrap
Framework].

The `./subtheme/sass/bootstrap.scss` file is nearly an exact copy from the
[Bootstrap Framework Source Files]. The only difference is that it injects the
`variable-overrides.scss` file directly after it has imported the[Bootstrap
Framework]'s `variables.scss` file. This allows you to easily override variables
without having to constantly keep up with newer or missing variables during an
upgrade.

The `./subtheme/sass/overrides.scss` file contains various Drupal overrides to
properly integrate with the [Bootstrap Framework]. It may contain a few
enhancements, feel free to edit this file as you see fit.

The `./subtheme/sass/style.scss` file is the glue that combines the
`bootstrap.scss` and `overrides.scss` files together. Generally, you will not
need to modify this file unless you need to add or remove files to be imported.
This is the file that you should compile to `./subtheme/css/styles.css` (note
the same file name, using a different extension of course).

## Override Theme Settings {#settings}

- TODO

## Override Templates and Theme Functions {#registry}

- TODO

[Bootstrap Framework]: http://getbootstrap.com
[Bootstrap Framework Source Files]: https://github.com/twbs/bootstrap-sass/releases
[SASS]: http://sass-lang.com/
