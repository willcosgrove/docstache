# Changelog

## 0.3.2
* [b3b66a0cd7ae67834cdbe7c18cefdb1498bcc5ab] I'm an idiot.  Fixed an error in the `Document#unusable_tags` method

## 0.3.1
* [2228ba727f8a2e3705fe223ce02b5e760c935572] Added `Document#unusable_tags` to list out tags that are not able to be interpolated due to being split across tags in the Document's XML

## 0.3.0
* [c841078f7d340c18323f05f0785e75cd560eed2c] Added ability to do tag interpolation in headers and footers.  The header/footer used is the header or footer from the first document passed into `Document.new()`

## 0.2.1
* [25b4c2e9e3dcb19b6fe9a255fec2c2bfd92029a6] Fixed a bug where a tag with regular expression characters could not be fixed with the `fix_errors` method

## 0.2.0

* [902d9890bee1a20a90377a94c3096a51781e8a24] You can access array elements with `[]`s within a `{{tag}}`
* [a36c4fefed763b6a54d15564e887fbcf3c3421e3] You can use conditions on loops to only loop over specific elements

## 0.1.0

* [08f09d1922e73ccaf17989a568deeb2ce0ebd4b8] Hash keys inside DataScope are symbolized

## 0.0.6

* [f945bc70ebb684f21e2488a3ad30c205bc05ddbb] Fixed a bug When two tags were inside one xml node, it would mistakenly report that there was an error when there wasn't.

## 0.0.5

* Fixed a bug that caused {{^tags}} to always show up as errors

## 0.0.4

* Rewrite of the Renderer class
* Conditional Blocks now work
* Loops now work

## 0.0.3

* Added ability to have nested tags like `{{purchase_order.number}}` through the
  use of the `Docstache::DataScope` class

## 0.0.2

* Fixed a bug that made appended documents not get appended to the *end* of a
  document
* Fixed a bug that made merged documents not open in Word.  This was caused due
  to the `section properties` tag in the xml getting used more than once, since
  each document had one.  Now only the first `sectPr` tag is kept.

## 0.0.1

* Initial release.  Still not working:
  * Nested tags `{{foo.bar}}`
  * Blocks (loops and conditiontals) `{{#foo}} ... {{/foo}}`
