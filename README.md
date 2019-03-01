# Mobile Chrome vh units fix

What is this?

Mobile (Android and iOS) Chrome has something I consider a bug. On scroll, when address bar dissapears, inner window height is changed, and with it vh units size is changed as well, making whole page to jump after recalculating the layout. This also happens when keyboard pops up.

This small library aims to solve that problem.

## Usage

**Options is an array of objects, every containing two attributes - CSS class and height in vh units.**

```javascript
    var vhFix = new VHChromeFix(options)

    var options = [
  {
    selector: '.Bears', // Mandatory, CSS selector
    vh: 150,  // Mandatory, height in vh units
  },
  {
    selector: '.Foxes',
    vh: 50
  },
  {
    selector: '.Horses',
    vh: 100
  }
];

var vhFix = new VHChromeFix(options);
```