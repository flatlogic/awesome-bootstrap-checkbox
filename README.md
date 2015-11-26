Awesome Bootstrap Checkbox
==========================

[Font Awesome][] [Bootstrap][] Checkboxes & Radios plugin. Pure CSS way to make inputs look prettier. **No Javascript!**

**[Demo][]**

Use
------------

First just include **awesome-bootstrap-checkbox.css** somewhere in your HTML, or add the equivalent files to your [Sass](#using-sass) / [Less](#using-less) configuration.
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

Credits
------------

Based on the [Official Bootstrap Sass port][Bootstrap Sass] and the awesome [Font Awesome][].


[Demo]: http://flatlogic.github.io/awesome-bootstrap-checkbox/demo/
[Bootstrap]: http://getbootstrap.com/
[Bootstrap Sass]: https://github.com/twbs/bootstrap-sass
[Font Awesome]: https://github.com/FortAwesome/Font-Awesome
[Glyphicons]: http://getbootstrap.com/components/#glyphicons
[Sass]: http://sass-lang.com/
[Less]: http://lesscss.org/
