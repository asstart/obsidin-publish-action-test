---
tags:
- random
---

### Features

Document contained examples of [GFM spec](https://github.github.com/gfm/#overview)

# Editor.md

## Thematic breaks

[A line consisting of 0-3 spaces of indentation, followed by a sequence of three or more matching -, _, or * characters, each followed optionally by any number of spaces or tabs, forms a thematic break.](https://github.github.com/gfm/#example-13)


>```
>***
>```
>***

>```
>---
>```
>---

>```
>___
>```
>___

[Wrong charactes](https://github.github.com/gfm/#example-14)

>```
>+++
>```
>+++

>```
>===
>```
>===

[Not enough characters](https://github.github.com/gfm/#example-16)

>```
>**
>```
>**

>```
>--
>```
>--

>```
>__
>```
>__

[One to three spaces indent are allowed](https://github.github.com/gfm/#example-17)

>```
> ***
>```
> ***

>```
>  ***
>```
>  ***

>```
>   ***
>```
>   ***

[Four spaces is too many](https://github.github.com/gfm/#example-18)

>```
>    ****
>```
>    ****

[More than three characters may be used](https://github.github.com/gfm/#example-20)

>```
>********
>```
>********

[Spaces are allowed between the characters and at the end](https://github.github.com/gfm/#example-21)

>```
> - - -
>```
> - - -

>```
> ** *   ** *
>```
> ** *   ** *

>```
>_ _ _   
>```
>_ _ _   

[Evene more then 4 spaces between](https://github.github.com/gfm/#example-23)

>```
>-    -    - -
>```
>-    -    - -
 
[No other characters may occur in the line](https://github.github.com/gfm/#example-25)

>```
>_ _ _ _ a
>```
>_ _ _ _ a

>```
>a------
>```
>a------

>```
>---a---
>```
>---a---

[It is required that all of the non-whitespace characters be the same](https://github.github.com/gfm/#example-26)

>```
> *-*
>```
> *-*

[When both a thematic break and a list item are possible interpretations of a line, the thematic break takes precedence](https://github.github.com/gfm/#example-30)

>```
>* Foo
>* * *
>* Bar
>```
>* Foo
>* * *
>* Bar

[If you want a thematic break in a list item, use a different bullet](https://github.github.com/gfm/#example-31)

>```
>- Foo
>- * * *
>```
>- Foo
>- * * *

## Headings

[Simple headings](https://github.github.com/gfm/#example-32)

>```
># foo
>## foo
>### foo
>#### foo
>##### foo
>###### foo
>```
># foo
>## foo
>### foo
>#### foo
>##### foo
>###### foo

[More than six # characters is not a heading](https://github.github.com/gfm/#example-33)

>```
>####### foo
>```
>####### foo

[At least one space is required between the # characters and the heading’s contents](https://github.github.com/gfm/#example-34)

>```
>#not heading
>```
>#not heading

[Not a heading, because the first # is escaped](https://github.github.com/gfm/#example-35)

>```
>\## not heading
>```
>\## not heading

[Contents are parsed as inlines](https://github.github.com/gfm/#example-36)

>```
># foo *bar* \*baz\*
>```
># foo *bar* \*baz\*

[Leading and trailing whitespace is ignored in parsing inline content](https://github.github.com/gfm/#example-37)

>```
>#                  foo                     
>```
>#                  foo                     

[One to three spaces indentation are allowed](https://github.github.com/gfm/#example-38)

>```
> ### foo
>  ## foo
>   # foo
>```
> ### foo
>  ## foo
>   # foo

[Four spaces are too much](https://github.github.com/gfm/#example-39)

>```
>    # foo
>```
>    # foo

[A closing sequence of # characters is optional](https://github.github.com/gfm/#example-41)

>```
>## foo ##
>  ###   bar    ###
>```
>## foo ##
>  ###   bar    ###

[It need not be the same length as the opening sequence](https://github.github.com/gfm/#example-42)

>```
># foo ##################################
>##### foo ##
>```
># foo ##################################
>##### foo ##

[Spaces are allowed after the closing sequence](https://github.github.com/gfm/#example-43)

>```
>### foo ###     
>```
>### foo ###     

[A sequence of # characters with anything but spaces following it is not a closing sequence, but counts as part of the contents of the heading](https://github.github.com/gfm/#example-44)

>```
>### foo ### b
>```
>### foo ### b

[The closing sequence must be preceded by a space](https://github.github.com/gfm/#example-45)

>```
># foo#
>```
># foo#

[Backslash-escaped # characters do not count as part of the closing sequence](https://github.github.com/gfm/#example-46)

>```
>### foo \###
>## foo #\##
># foo \#
>```
>### foo \###
>## foo #\##
># foo \#

## Setext headings

[Simple examples](https://github.github.com/gfm/#example-50)

>```
>Foo *bar*
>=========
>```
>Foo *bar*
>=========

>```
>Foo *bar*
>---------
>```
>Foo *bar*
>---------

[The content of the header may span more than one line](https://github.github.com/gfm/#example-51)

>```
>  Foo *bar
>baz*→
>====
>```
>  Foo *bar
>baz*→
>====

[The underlining can be any length](https://github.github.com/gfm/#example-53)

>```
>Foo
>-------------------------
>```
>Foo
>-------------------------

>```
>Foo
>=
>```
>Foo
>=

[The heading content can be indented up to three spaces, and need not line up with the underlining](https://github.github.com/gfm/#example-54)

>```
>   Foo
>---
>```
>   Foo
>---

>```
>  Foo
>-----
>```
>  Foo
>-----

>```
>  Foo
>  ===
>```
>  Foo
>  ===

[The setext heading underline cannot contain internal spaces](https://github.github.com/gfm/#example-58)

>```
>Foo
>= =
>```
>Foo
>= =

[A blank line is needed between a paragraph and a following setext heading, since otherwise the paragraph becomes part of the heading’s content](https://github.github.com/gfm/#example-65)

>```
>Foo
>Bar
>---
>```
>Foo
>Bar
>---

[Blank line is not required before or after setext headings](https://github.github.com/gfm/#example-66)

>```
>---
>Foo
>---
>Bar
>---
>Baz
>```
>---
>Foo
>---
>Bar
>---
>Baz

[Setext headings cannot be empty](https://github.github.com/gfm/#example-67)

>```
>
>====
>```
>
>====

