## Changelog for the `threepenny-gui` package

**0.6.0.3** -- Maintenance release.

* Temporary fix for #109, which was causing event handlers to be discarded.

**0.6.0.2** -- Maintenance release.

* Remove unused direct dependencies, in particular
** attoparsec-enumerator
** utf8-string
** MonadCatchIO-transformers
** time

**0.6.0.1** -- Maintenance release.

* The `ADDR` environment variable is now parsed correctly.
* Now builds on GHC 7.8 and GHC 7.10
* The example source code in the `samples` folder has been reorganized and consolidated.

**0.6.0.0** -- Snapshot release.

* The internals of the JavaScript FFI has been reimplemented completely. A new module `Foreign.JavaScript` exports a bare JavaScript FFI in case you want to write a custom GUI framework. However, the module `Graphics.UI.Threepenny` is *not* compatible with it, even though it builds on top of it.
* The fields of `Config` type for server configuration are now prefixed with `js` instead of `tp`. Example: `jsPort`, `jsStatic`.
* The functions `loadFile` and `loadDirectory` have been *removed*, as I felt that the `jsStatic` option is sufficient for most use cases.

**0.5.0.0** -- Snapshot release.

* Possibility to specify IP address to bind the server to.
* FFI now supports callbacks into Haskell. Remove `callDeferredFunction` function.
* `Graphics.UI.Threepenny.Canvas.SVG` for creating SVG elements and attributes.
* 2D graphics API in `Graphics.UI.Threepenny.Canvas` is beginning to grow.
* `Bool` is now correctly marshalled to JavaScript.
* `Text` can now be marshalled to JavaScrtip.

**0.4.2.0** -- Maintenance release.

* Dependency `bytestring >=0.9.2` is now implemented correctly.
* Allow newer versions of `aeson` dependency.
* Allow newer versions of `network`, `transformers` and `template-haskell` dependencies.
* Helper scripts in the `samples` directory now assume that you use a cabal sandbox for development.
* The `UI` monad is now an instance of the `Applicative` class.

**0.4.1.0** -- Maintenance release.

* Dependency on `text` package now from version 0.11 to 1.1.*.
* Dependency on `aeson` package replaces the former dependency on the `json` package.
* Unicode characters are now transmitted correctly to the browser. #75, #62.
* Change default port number to 8023. #64

**0.4.0.2** -- Bugfix release.

* Fix CSS bug for `grid` function.

**0.4.0.1** -- Maintenance release.

* Adjust package dependencies.

**0.4.0.0** -- Snapshot release.

* New `UI` monad for easier JavaScript FFI and recursion in FRP.
* Garbage collection for DOM elements. (Unfortunately, this doesn't support using custom HTML files anymore, see [issue #60][60].)
* First stab at widgets.
* Update dependency to `websockets-0.8`.

**0.3.0.0** -- Snapshot release.

* Browser communication with WebSockets.
* First stab at FRP integration.

**0.2.0.0** -- Snapshot release.

* First stab at easy JavaScript FFI.

**0.1.0.0**

* Initial release.



  [60]: https://github.com/HeinrichApfelmus/threepenny-gui/issues/60