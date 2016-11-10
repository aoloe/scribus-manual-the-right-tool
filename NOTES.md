# Notes

## Which version?

https://sourceforge.net/projects/scribus/files/

diese versionen sind alle vom team zu verfügung gestellt und bauen auf einander.

zuerst ein paar fakten:

- scribus-svn sind snapshots, das heisst binaries die an einen "zufallstag" erstellt wurden
- scribus-devel sind "entwickler"-versionen, das heisst binaries, die dann erzeugt werden, wenn gewisse zwicschenziele erreicht wurden 
- scribus-lib sind die libraries die du brauchen kannst, um scribus unter windows (mit msvc) zu kompieleren
- in scribus sind die stabile versionen von scribus

und nun meine meinungen:

grundsätzlich, sollte jemand die neuste version in scribus/ gebrauchen.

- scribus-svn macht es möglich, unter windows (und zum teil mac) die letzte korrekturen zu testen.
- scribus-devel ist für neugierige angsthasen, die zu faul sind um scribus zu kompilieren aber doch nicht mit stable arbeiten möchten.
- https://github.com/scribusproject/scribus und svn://scribus.net/trunk/Scribus sind für die die es wagen, immer auf dem laufend zu sein.

persönlich kann ich empfehlen, entweder mit der stabile version oder mit der git/svn-version zu arbeiten.
die andere sind ein bisschen ein risiko, da sie bugs haben können, die nur langsam dann korrigiert werden (erst beim nächsten upload).
(und wenn jemand es nicht schafft, scribus zu kompilieren, der wird vermutlich auch nicht den geduld haben, mit eine entwicklerversion zu arbeiten).
aber es gibt leute die glücklich mit den scribus-devel versionen arbeiten.

### Currently suggested versions

At the time of writing (10.11.2016) you should use one of the following versions:

- The stable version, Scribus 1.4.6: if you're starting with Scribus or you're sharing your files with other Scribus users. Or if you don't have good reasons for using something else.
- The latest development release, Scribus 1.5.2:
  - If you have been using Scribus for some time and hit some issues that you know have been solved in the development version.
  - If you you're evaluation Scribus for future use (but you should also evaluate 1.4, since the release date for 1.6 is still unknown).
  - If you are used to work with unstable programs and are ready to write bug reports to help the developers improve Scribus.
- The current development code (svn, git):
  - If you're contributing to the Scribus development.
  - If you need features that have been added very recently.
  - In the near future, it's very likely that the merge of the CTL branch will make the development version unstable.
- The Scribus CTL branch
  - Don't use it in production. Ever.
  - If you want to test how well your language and OTF features are supported.
  - If you want to test the speed improvements.

## Where to get Scribus?

### Scribus for Windows

### Scribus for OS X

### Scribus for Linux

### Scribus for other OSes

## Juggling between multiple versions of Scribus

### Installing multiple versions on the same computer

### Work with 1.4, export the PDFs with 1.5

### Only selected projects with 1.5

## Key features and dangers of each version

### Scribus 1.4

### Scribus 1.5.2

- _Footnotes_ and marks: don't use them in production.
- _Tables_: in most cases, not worth to be used (import SVG/PNG from Libreoffice; use tabulators).
- The UX in the _properties palette_ is mostly broken (scrolling with the mouse wheel changes field values; lot of scrolling needed).
- The _Undo_: use it if care. If you get strange results, close the file without saving. If you can replicate strange, please report the bug with the steps to replicate. 
- _Importing PDF files_: should work well.
- _Drop shadoows_: can make Scribus very slow.
- _Layers_: there might still be a bug that makes Scribus slow if you have multiple pages and more than one layer.
- _Orphan and Widows_
- _Bullet / Numerated Lists_: use with care; if you hit issues, report them and use indents + tabulators
- _Transparency and Gradients_: much improved support
- _Patterns_ (updatable Scrapbook elements)
- "Dynamic" text frame chaining and advanced chain breaking.
- Import multiple text or vector items at a time.
- _"Welding"_: relative position between items (hard to grock; limited functionality; not tested in production yet)
- _Snap to Items_

### Scribus 1.5.3svn

The remarks concerning 1.5.2 are also valid for 1.5.3svn, except if spefically noted.

- Footnotes: please test the improvements, but use in production with much care

### Scribus 1.5.3 CTL

- Don't use it in production.
- Complex Text Lyout (CTL): full support for CTL languages is being implemented. We need tests with Arabic, Indic and CJK languages.
- OTF features (ligatures, stylistic alternates, ...)

Please write bug reports to https://github.com/HOST-Oman/scribus/issues
