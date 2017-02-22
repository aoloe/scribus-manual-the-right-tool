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

you can use a stable and a development version of scribus alongside on the same machine.

but the file you have saved with 1.5 won't open anymore with 1.4.  
only work on backups of existing files or be ready to start from scratch 

### Using a development version

In most cases, if you're using a development version, you should try to keep your software up to date.

But you should always keep a copy of the last version of Scribus you know did work for you.

Generally speaking, new versions of scribus can read older files.  
The upgrade from 1.5.2 to 1.5.3 has an exception (that will probably still be true when 1.6 will be released): text  in documents created with older versions of Scribus can look different.  
But -- most of the time -- older versions cannot read files created with newer versions.

## Where to get Scribus?

### Scribus for Windows

#### The latest released development snapshot

#### The current development version

https://sourceforge.net/projects/scribus/files/scribus-svn/1.5.3.svn/

### Scribus for OS X

#### The latest released development snapshot

#### The current development version

https://sourceforge.net/projects/scribus/files/scribus-svn/1.5.3.svn/

### Scribus for Linux

#### Getting the current development version

For Ubuntu:

https://launchpad.net/~scribus/+archive/ubuntu/ppa

For most linuxes:

https://bintray.com/probono/AppImages/Scribus

An AppImage is a container that contains all what is needed to run Scribus on your Linux computer: Download it, make it executable and run it.

See the Appimage website for more details: http://appimage.org/  
Or (this longer Stackoverflow article](http://askubuntu.com/questions/774490/what-is-an-appimage-how-do-i-install-it)

Notes:

- You might need to set `$PYTHONHOME` to your local python install (as an example in a script that will first set the value and then launch the appimage).


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

## Editing a PDF

Scribus can read PDF files but is not a PDF editor.  
It's not the right tool for tweaking little bits of text in a PDF.

Also, PDF is not a format that is meant to be further edited.  
But, if I had to modify one, I would first try Inkscape.  
Then LibreOffice Writer / Draw.  
In the past I've used flpsed, but i'm not sure I would still use it.

That being said:

- If you're using a stable Scribus 1.4.x, all you can do is:
  - load the PDF as a background image on a page (put a full page image frame behind everything),
  - cover the old text with a white rectangle and
  - retype the text.

  Slightly better than tipexing on paper.

- If you're working with a development Scribus 1.5.x (or later)
  - you can load the PDF page as a vector,
  - remove the old text and
  - type the new text.

  But
  - The text will always be vectorized on import (no real editing is possible) and
  - it won't reflow.

