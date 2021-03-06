# ModalJS
ModalJS - Enjoy experience with custom modals.

##[Live example](http://pdknight.github.io/ModalJS/src/example/)

# Install
1. Download latest zipped (.zip) version of repository.
2. That's it! Now you can use Modal.js and Modal.css files wherever you want!

# Files
* **Modal.js**
  * Core library.
* **Modal.css**
  * Additive CSS styles for custom modals.

# How to create a modal
You can create a modal with `ModalJS.show` function:
```javascript
ModalJS.show({
    top: 'Modal title.',
    middle: 'Modal body.'
});
```
`top` and `middle` are required properties. You can also use some of list below:
* type: modal, success, alert, warning, error
* transition: fast, normal, slow
* mono: false, true
* background: false, true
* size: small, medium, big
* position: stickedToTop, top, middle, bottom, stickedToBottom

```javascript
ModalJS.show({
    top: 'To install our product you need to agree with our example license.',
    middle: 'The MIT License (MIT)<br>Copyright (c) &lt;year&gt; &lt;copyright holders&gt;<br><br>License...',
    size: 'big',
    transition: 'slow',
    confirm: {
        text: 'I agree.',
        click: function() {
            alert('Thank you!');
        }
    }
});
```

# Custom `Array` and `Node` functions
##### Array.prototype.contains(element)
Returns true if array contains an element.
* **element**: an element.

##### Node.prototype.removeClasses(classes)
Removes classses from node.
* **classes**: array of strnigs representing classes themselves.

##### Node.prototype.addClass(c)
Adds class to an element.
* **c**: class, a string.

# ModalJS functions and variables
> **Tip**: You can use `modaljs` or `ModalJS` variable.

##### ModalJS.version
Returns current ModalJS version.

##### ModalJS.modal(type)
Returns element of modal depending on element:
* bg
* modals
* modal
* top
* topCancel
* middle
* bottom
* bottomCancel
* bottomConfirm
* transitionType

##### ModalJS.isShown()
Returns `tru` (modal is shown) or `false` (modal is hidden)

##### ModalJS.sel(selector [, all])
Returns an element or group of elements depending on selector.
* **selector**: Query selector.
* **all (optional)**: true (select all occurencies) or false (select first occurence).

##### ModalJS.addEvent(el, name, func)
Applies event function on an element(s).
* **el**: Element (or group of elements) to have event applied on.
* **name**: Name of element (`Without 'on'!`).
* **func**: A function that is executed on current event.

##### ModalJS.init(props)
Initializes modal with default properties.
* **props**: Default properties.

##### ModalJS.show(props)
Shows up a modal with custom properties.
* **props**: Custom properties.

##### ModalJS.showModal()
Shows modal.

##### ModalJS.hideModal()
Hides modal.
