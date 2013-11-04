# Sass Prefixer (Beta)

Sass-prefixer is a vendor prefixer for sass written in scss, you only need to download sass-prefixer.scss, import the file in your scss and start using it. That's all! Sass-prefixer it's in beta version, it  but it works well with almost all common css properties.


### Quick start

* [Download sass-prefixer](https://raw.github.com/Aloge/sass-prefixer/master/_sass-prefixer.scss)
* Save the file in your project directory, inside the scss folder (recommended)
* Import sass-prefixer in your main scss file. If you don't have the sass-prefixer file in the same path as your scss main file you need to specify a relative path.

```
// Import sass-prefixer
@import "sass-prefixer";
```
* Once you've imported sass-prefixer, you only need to include the mixin into your code to prefix your styles. This is the way to do:

```
// This is a selector with unprefixed properties
.unprefixed {
	box-sizing: border-box;
}

// This is a selector with prefixed properties using sass prefixer
// sass-prefixer mixin use only two parameter, the first for the css property
// and the second for the css value: @include prefix($property,$value), you
// should introduce the two parameters to avoid create an error while the scss
// file is compiling.
.prefixed {
	@include prefix(box-sizing, border-box)
}

```
This code compiles to:
```
.unprefixed {
	box-sizing: border-box;
}

.prefixed {
	-moz-box-sizing: border-box;
	-webkit-box-sizing: border-box;
	box-sizing: border-box;
}
```

### Customize it

You can specify what browsers you want sass-prefixer support modifying the $prefixer-web-browsers-support variable in sass-prefixer.scss or adding it in your scss with a different value


### Bugs and feature requests

Have a bug or a feature request? [Please open a new issue](https://github.com/aloge/sass-prefixer/issues). Before opening any issue, please search for existing issues and read the [Issue Guidelines](https://github.com/aloge/CONTRIBUTING.md#using-the-issue-tracker), written by [Nicolas Gallagher](https://github.com/necolas/).


### Contributing

Please read through the [contributing guidelines](https://github.com/aloge/CONTRIBUTING.md). Included are directions for opening issues, coding standards, and notes on development.


### Author

**[Alex Guerrero](https://github.com/Aloge)**


### License

Public License (Unlicense)