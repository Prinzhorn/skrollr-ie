skrollr-ie
==========

skrollr plugin that adds some missing features to IE < 9

The plugin makes IE understand `opacity`, `rgb()` and `hsl()` (the ones with alpha are mapped to them) and it creates a very simple `document.querySelector` polyfill which only supports ID selectors (using `getElementById`). Needed if you want to use [data-anchor-target](https://github.com/Prinzhorn/skrollr#relative-mode-or-viewport-mode).

Documentation
=====

Include `dist/skrollr.ie.min.js` after the core using conditional comments.

```html
<script type="text/javascript" src="skrollr.min.js"></script>

<!--[if lt IE 9]>
<script type="text/javascript" src="skrollr.ie.min.js"></script>
<![endif]-->
```


Changelog
====

1.0.3 (2014-04-30)
------------------

* Fixed issues with opacity. The filter is now getting removed when opacity is 1 (#4).

1.0.2 (2013-11-24)
------------------

* Reverted #3. Leaving the opacity filter on the element even with 100% keeps it from getting anti-aliasing (#1).

1.0.1 (2013-11-16)
------------------

* Don't remove the opacity when it reaches 1 (#1, #3).

1.0.0 (2013-05-18)
------------------

* Moved skrollr-ie to a dedicated repo.