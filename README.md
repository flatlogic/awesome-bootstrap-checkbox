# 🤘 Awesome Bootstrap Checkbox

[![NPM version](https://img.shields.io/npm/v/awesome-bootstrap-checkbox.svg?style=flat)](https://www.npmjs.com/package/awesome-bootstrap-checkbox)
[![NPM downloads](https://img.shields.io/npm/dm/awesome-bootstrap-checkbox.svg?style=flat)](https://www.npmjs.com/package/awesome-bootstrap-checkbox)
[![Dependency Status](https://img.shields.io/david/dev/flatlogic/awesome-bootstrap-checkbox.svg?branch=master&style=flat)](https://www.npmjs.com/package/awesome-bootstrap-checkbox)
[![Join the chat at https://gitter.im/flatlogic/awesome-bootstrap-checkbox](https://badges.gitter.im/flatlogic/awesome-bootstrap-checkbox.svg)](https://gitter.im/flatlogic/awesome-bootstrap-checkbox?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

[View Demo](http://flatlogic.github.io/awesome-bootstrap-checkbox/demo/) | [Download](https://github.com/flatlogic/awesome-bootstrap-checkbox.git) | [More templates](https://flatlogic.com/templates) | [Support forum](https://flatlogic.com/forum)

[Font Awesome][] [Bootstrap][] Checkboxes & Radios plugin. Pure CSS way to make inputs look prettier. **No Javascript!**

For **[Bootstrap 4 version](https://getbootstrap.com/docs/4.6/getting-started/introduction/)** please checkout [bump-to-bootstrap4][] branch

For **[Bootstrap 5 version](https://getbootstrap.com/)** please checkout [bump-to-bootstrap5](https://github.com/flatlogic/awesome-bootstrap-checkbox/tree/bump-to-bootstrap5) branch

Check out our React/Vue/Angular/Node.js boilerplates
-----------
[Flatlogic Templates](https://flatlogic.com/templates) - 💥Free and open-source application boilerplates built with Bootstrap 5, React, Vue, Angular, Node.js

Use
------------

To install latest version via NPM simply run:
```shell
$ npm install awesome-bootstrap-checkbox # for Bootstrap 4 version
$ npm install awesome-bootstrap-checkbox@0.3.7 # for Bootstrap 3 version
```

There is a separate [README.md][] file for **[Bootstrap 4 version][]**.

Then just include **awesome-bootstrap-checkbox.css** somewhere in your HTML, or add the equivalent files to your [Sass](#using-sass) / [Less](#using-less) configuration.
Next, everything is based on code convention. Here is checkbox markup from Bootstrap site:

````html
<form role="form">
  ...
  <div class="checkbox">
    <label>
      <input type="checkbox"> Check me out
    </label>
  </div>
  ...
</form>
````

We have to alter it a bit:
````html
<form role="form">
  ...
  <div class="checkbox">
    <input type="checkbox" id="checkbox1">
    <label for="checkbox1">
        Check me out
    </label>
  </div>
  ...
</form>
````
That's it. It will work. But it **will not** work if you nest input inside label or put label before input.

If you want to enable **Opera 12** and earlier support  just add class `styled` to `input` element:
````html
...
<input type="checkbox" id="checkbox1" class="styled">
...
````

Browser support
-----------
- Firefox (_3.6+_)
- Chrome  (_14+_)
- IE      (_9+_)
- Opera   (_11.6+_)
- Safari  (_6+_)

Radios
------------

It's the same for radios. Markup has to be the following:
````html
<form role="form">
  ...
  <div class="radio">
      <input type="radio" name="radio2" id="radio3" value="option1">
      <label for="radio3">
          One
      </label>
  </div>
  <div class="radio">
      <input type="radio" name="radio2" id="radio4" value="option2" checked>
      <label for="radio4">
          Two
      </label>
  </div>
  ...
</form>
````

Brand Colors and other features
------------

You may use `checkbox-primary`, `checkbox-danger`, `radio-info`, etc to style checkboxes and radios with brand bootstrap colors.

`checkbox-circle` is for rounded checkboxes.

Inputs without label text:

````html
<div class="checkbox">
  <input type="checkbox" class="styled" id="singleCheckbox1" value="option1" aria-label="Single checkbox One">
  <label></label>
</div>
````

Using [Sass][]
----------

As per example in the `demo` folder, to use Font Awesome you'll have to `@import` the following library parts:

````scss
@import "../bower_components/bootstrap-sass-official/assets/stylesheets/bootstrap/variables";
@import "../bower_components/bootstrap-sass-official/assets/stylesheets/bootstrap/mixins";

@import "../bower_components/Font-Awesome/scss/variables";

@import "../awesome-bootstrap-checkbox";
````

Adjust this to the path where your bootstrap and font-awesome files are located.

Using [Less][]
----------

Just like the Sass setup, you'll have to `@import` the following library parts:

````less
@import "../bower_components/bootstrap/less/variables";
@import "../bower_components/bootstrap/less/mixins";

@import "../awesome-bootstrap-checkbox";

@import "../bower_components/Font-Awesome/less/variables";
````

Custom icon font
------------

If you want to use another icon font instead of Font Awesome, such as [Glyphicons][], override the default variables:
````scss
$font-family-icon: 'Glyphicons Halflings';
$check-icon: "\e013";

.checkbox label:after {
    padding-left: 4px;
    padding-top: 2px;
    font-size: 9px;
}
````

or for Less:
````less
@font-family-icon: 'Glyphicons Halflings';
@check-icon: "\e013";

// Same styles as the Sass example...
````

Or for plain CSS, override the `.checkbox` class (and `.styled` class for Opera):
````css
input[type="checkbox"].styled:checked + label:after,
input[type="radio"].styled:checked + label:after,
.checkbox input[type=checkbox]:checked + label:after {
    font-family: 'Glyphicons Halflings';
    content: "\e013";
}

input[type="checkbox"].styled:checked label:after,
input[type="radio"].styled:checked label:after,
.checkbox label:after {
    padding-left: 4px;
    padding-top: 2px;
    font-size: 9px;
}
````

How can I support developers?
------------------------------
- Star our GitHub repo :star:
- Create pull requests, submit bugs, suggest new features or documentation updates :wrench:
- Follow us on [Twitter](https://twitter.com/flatlogic) :feet:
- Like our page on [Facebook](https://www.facebook.com/flatlogic/) :thumbsup:

Support
------------------------------
For any additional information please go to our [**support forum**](https://flatlogic.com/forum) and raise your questions or feedback provide there. We highly appreciate your participation!

More from Flatlogic
------------------------------
- [React Native Starter](https://flatlogic.com/templates/react-native) - 🚀 A powerful react native starter template that bootstraps development of your mobile application 
- [Sing App Dashboard](https://flatlogic.com/templates/sing-app-html5) - 💥 Free and open-source admin dashboard template built with Bootstrap 4
- [React Material Admin](https://flatlogic.com/templates/react-material-admin-full) - ⚡ Admin boilerplate made with React 17 and Material-UI 5

Credits
------------

Based on the [Official Bootstrap Sass port][Bootstrap Sass] and the awesome [Font Awesome][].


[Demo]: http://flatlogic.github.io/awesome-bootstrap-checkbox/demo/
[Bootstrap]: http://getbootstrap.com/
[Bootstrap 4 version]: https://getbootstrap.com/
[bump-to-bootstrap4]: https://github.com/flatlogic/awesome-bootstrap-checkbox/tree/bump-to-bootstrap4
[Bootstrap Sass]: https://github.com/twbs/bootstrap-sass
[Font Awesome]: https://github.com/FortAwesome/Font-Awesome
[Glyphicons]: http://getbootstrap.com/components/#glyphicons
[Sass]: http://sass-lang.com/
[Less]: http://lesscss.org/
[README.md]: https://github.com/flatlogic/awesome-bootstrap-checkbox/tree/bump-to-bootstrap4
