# Inert Bug 1

https://bugs.chromium.org/p/chromium/issues/detail?id=1354313

Accessiblity tree breaks on some interaction between CSS `content-visibility: auto;` and the `inert` attribute.

https://romainmenke.github.io/inert-bug-1/

Before toggling `inert`

<img width="476" alt="Screenshot 2022-08-19 at 18 15 50" src="https://user-images.githubusercontent.com/11521496/185662432-f02a8bb4-c4f6-4707-a72b-3e33c28929ed.png">

After toggling `inert`

<img width="480" alt="Screenshot 2022-08-19 at 18 15 56" src="https://user-images.githubusercontent.com/11521496/185662441-7f1d8c39-78da-41e7-afd4-0346f159c6b8.png">

- Expected behavior is that the accessibility tree is the same before and after clicking the button twice.
- Actual behavior is that some elements remain ignored.

----------------

https://romainmenke.github.io/inert-bug-1/index-b.html

This variant doesn't use `inert` but instead uses a class and `display: none;` to exclude/include elements from the accessiblity tree.

----------------

https://romainmenke.github.io/inert-bug-1/index-c.html

This variant doesn't use `content-visibility: auto` but instead uses `hidden` and `visible` explicitly.
