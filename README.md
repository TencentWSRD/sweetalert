SweetAlert [![Build Status](https://travis-ci.org/t4t5/sweetalert.svg?branch=master)](https://travis-ci.org/t4t5/sweetalert)
==========

An awesome replacement for JavaScript's alert.

#### ATTENTION!

This is a private usage version for our project RDM-CI. Forked from `sweetalert@1.1.3`.

#### 注意！

这是一个专门针对团队内部的sweetalert版本，为了解决bootstrap-sweetalert的fork版本过低导致无法使用一些新特性的问题，对sweetalert做了修改使之与`bootstrap-sweetalert`的行为一致。

![A success modal](https://raw.github.com/t4t5/sweetalert/master/sweetalert.gif)


Usage
-----

Through npm:

```bash
npm install sweetalert-ci-dev
```

Alternatively, download the package and reference the JavaScript and CSS files manually:

```html
<script src="dist/sweetalert.min.js"></script>
<link rel="stylesheet" type="text/css" href="dist/sweetalert.css">
```

Tutorial
--------

The easiest way to get started is follow the [SweetAlert tutorial on Ludu](https://www.ludu.co/lesson/how-to-use-sweetalert)!


Examples
--------

The most basic message:

```javascript
swal("Hello world!");
```

A message signaling an error:

```javascript
swal("Oops...", "Something went wrong!", "error");
```

A warning message, with a function attached to the "Confirm"-button:

```javascript
swal({
  title: "Are you sure?",
  text: "You will not be able to recover this imaginary file!",
  type: "warning",
  showCancelButton: true,
  confirmButtonClass: "btn-danger",
  confirmButtonText: "Yes, delete it!",
  closeOnConfirm: false,
  html: false
}, function(){
  swal("Deleted!",
  "Your imaginary file has been deleted.",
  "success");
});
```

A prompt modal where the user's input is logged:

```javascript
swal({
  title: "An input!",
  text: 'Write something interesting:',
  type: 'input',
  showCancelButton: true,
  closeOnConfirm: false,
  animation: "slide-from-top"
}, function(inputValue){
  console.log("You wrote", inputValue);
});
```

Ajax request example:

```javascript
swal({
  title: 'Ajax request example',
  text: 'Submit to run ajax request',
  type: 'info',
  showCancelButton: true,
  closeOnConfirm: false,
  disableButtonsOnConfirm: true,
  confirmLoadingButtonColor: '#DD6B55'
}, function(inputValue){
  setTimeout(function() {
    swal('Ajax request finished!');
  }, 2000);
});
```

[View more examples](http://t4t5.github.io/sweetalert)


Themes
------

SweetAlert can easily be themed to fit your site's design. SweetAlert comes with three example themes that you can try out: **facebook**, **twitter** and **google**. They can be referenced right after the intial sweetalert-CSS:
```html
<link rel="stylesheet" href="dist/sweetalert.css">
<link rel="stylesheet" href="themes/twitter/twitter.css">
```


Browser compatibility
---------------------

SweetAlert works in most major browsers (yes, even IE). Some details:

- **IE8**: (Dropped since v1.0.0-beta)
- **IE9**: Works, but icons are not animated.
- **IE10+**: Works!
- **Safari 4+**: Works!
- **Firefox 3+**: Works!
- **Chrome 14+**: Works!
- **Opera 15+**: Works!


Contributing
------------

If you want to contribute:

- Fork the repo

- Make sure you have [Node](http://nodejs.org/), [NPM](https://www.npmjs.com/) and [Gulp](http://gulpjs.com/) installed. When in the SweetAlert directory, run `npm install` to install the dependencies. Then run `gulp` while working to automatically minify the SCSS and JS-files.

- Keep in mind that SweetAlert uses Browserify in order to compile ES6-files. For easy debugging, make sure you reference the file `dist/sweetalert-dev.js` instead of `sweetalert.js`.

- After you're done, make a pull request and wait for approval! :)
