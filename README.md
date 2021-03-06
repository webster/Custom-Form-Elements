# Custom Form Elements

![Maintained?](http://stillmaintained.com/karbassi/Custom-Form-Elements.png)

A lightweight custom form styler for radio, checkbox and select elements. Radio and Checkboxes have four states rather than just two.

Developed by [Ali Karbassi](http://karbassi.com).

This project lives on GitHub: [http://github.com/karbassi/Custom-Form-Elements](http://github.com/karbassi/Custom-Form-Elements)

This whole project is licensed under the MIT License: [http://karbassi.mit-license.org](http://karbassi.mit-license.org)

## Tested Environments

### Desktop

* Firefox 3.5+
* Chrome 10+

### Mobile

* iPhone 4 w/ iOS 5.1
* iPad w/ iOS 5.1

## Requirements

* Requires [jQuery 1.7+](http://jquery.com)
* All `form` elements require `id`s.

## Note

* Call once your document is loaded.
* If you are dynamically loading content, use the `repaint` function.

## Demo

[http://karbassi.github.com/Custom-Form-Elements/demo.html](http://karbassi.github.com/Custom-Form-Elements/demo.html)

## Example

### CSS

```css
.cfe-radio,
.cfe-checkbox,
.cfe-select,
.cfe-file {
    display: inline-block;
    cursor: pointer;
    background: 0 0 no-repeat;
}

.cfe-radio,
.cfe-checkbox {
    -webkit-tap-highlight-color: rgba(0,0,0,0);
}

.cfe-radio {
    background: url(radios.png);
    width: 12px;
    height: 11px;
}

.cfe-radio.cfe-state-0 { background-position: 0 0; }
.cfe-radio.cfe-state-1 { background-position: 0 -11px; }
.cfe-radio.cfe-state-2 { background-position: 0 -22px; }
.cfe-radio.cfe-state-3 { background-position: 0 -33px; }

.cfe-checkbox {
    background: url(checkbox.png);
    width: 12px;
    height: 12px;
    padding: 0;
}

.cfe-checkbox.cfe-state-0 { background-position: 0 0; }
.cfe-checkbox.cfe-state-1 { background-position: 0 -12px; }
.cfe-checkbox.cfe-state-2 { background-position: 0 -24px; }
.cfe-checkbox.cfe-state-3 { background-position: 0 -36px; }

.cfe-select,
.cfe-file {
    font: 10px/21px arial,sans-serif;
    color: #8A7967;
    overflow: hidden;
    position: absolute;
    padding: 0 24px 0 11px;
    width: 126px;
    height: 21px;
}

.cfe-select {
    background: url(select.png);
}

select.cfe-styled {
    position: relative;
    width: 161px;
}

.cfe-file {
    background: url(file.png);
}

/* Disabled style */
.cfe-disabled,
.cfe-readonly {
    /* IE 8 */
    -ms-filter: "progid:DXImageTransform.Microsoft.Alpha(Opacity=50)";

    /* IE 5-7 */
    filter: alpha(opacity=50);

    /* CSS3 */
    opacity: 0.5;
}
```

### Javascript

```javascript
jQuery(document).ready(function($) {

    // Default settings apply.
    // All input/select tags with a class of 'cfe-styled' are affected.
    var cf = new CustomFormElements();

    // All options
    var cf = new CustomFormElements({
        cssClass: 'styled'
    });

    // If you need to reinitialize dynamically added form elements:
    cf.repaint();

});
```
