---
layout: post
title: "Markdown Cheatsheet"
date: 2018-06-02 16:45:00 +0700
categories: markdown cheatsheet
description: markdown, markdown cheatsheet, markdown quick tutorial
---
## <span style="color:seagreen">Heading</span>
------

``` markdown
# Heading 1
## Heading 2
### Heading 3
```

# Heading 1
## Heading 2
### Heading 3

Probably, we often use heading until the third level. Beyond that, it's rarely used.

## <span style="color:seagreen">Emphasis</span>
------

``` markdown
_display text in italic_

**display text in bold**

**_display text in bold and italics_**

~~strikethrough~~
```

_display text in italic_

**display text in bold**

**_display text in bold and italics_**

~~strikethrough~~

## <span style="color:seagreen">Lists</span>
------
Four dots mean four space  
Two dots mean two space  

``` markdown
1. First ordered list item
2. Another item
....* Unordered sub-list. 
1. Actual numbers don't matter, just that it's a number
....1. Ordered sub-list
4. And another item.

   You can have properly indented paragraphs within list items. Notice the blank line above, and the leading spaces (at least one, but we'll use three here to also align the raw Markdown).

....To have a line break without a paragraph, you will need to use two trailing spaces..
....Note that this line is separate, but within the same paragraph..
....(This is contrary to the typical GFM line break behaviour, where trailing spaces are not required.)

* Unordered list can use asterisks
- Or minuses
+ Or pluses
```

1. First ordered list item
2. Another item
    * Unordered sub-list. 
1. Actual numbers don't matter, just that it's a number
    1. Ordered sub-list
4. And another item.

    You can have properly indented paragraphs within list items. Notice the blank line above, and the leading spaces (at least one, but we'll use three here to also align the raw Markdown).

    To have a line break without a paragraph, you will need to use two trailing spaces  
    Note that this line is separate, but within the same paragraph  
    (This is contrary to the typical GFM line break behaviour, where trailing spaces are not required.)

* Unordered list can use asterisks
- Or minuses
+ Or pluses

## <span style="color:seagreen">Link</span>
------

``` markdown
[I'm an inline-style link](https://www.inlinestyle.com)

[I'm an inline-style link with title](https://www.inlinestylewithtitle.com "Inline Style with Title's Homepage")

[I'm a reference-style link][Arbitrary case-insensitive reference text]

[I'm a relative reference to a repository file](../blob/master/LICENSE)

[You can use numbers for reference-style link definitions][1]

Or leave it empty and use the [link text itself].

URLs and URLs in angle brackets will automatically get turned into links. 
http://www.examplelink.com or <http://www.examplelink.com> and sometimes 
examplelink.com (but not on Github, for example).

Some text to show that the reference links can follow later.

[arbitrary case-insensitive reference text]: https://www.referenceetext.org
[1]: http://referencenumber.org
[link text itself]: http://www.textitself.com
```

[I'm an inline-style link](https://www.inlinestyle.com)

[I'm an inline-style link with title](https://www.inlinestylewithtitle.com "Inline Style with Title's Homepage")

[I'm a reference-style link][Arbitrary case-insensitive reference text]

[I'm a relative reference to a repository file](../blob/master/LICENSE)

[You can use numbers for reference-style link definitions][1]

Or leave it empty and use the [link text itself].

URLs and URLs in angle brackets will automatically get turned into links. 
http://www.examplelink.com or <http://www.examplelink.com> and sometimes 
examplelink.com (but not on Github, for example).

Some text to show that the reference links can follow later.

[arbitrary case-insensitive reference text]: https://www.referenceetext.org
[1]: http://referencenumber.org
[link text itself]: http://www.textitself.com

## <span style="color:seagreen">Code Container</span>
------

``` markdown
    inline `code`

    ```javascript
    var s = "JavaScript syntax highlighting";
    alert(s);
    ```

    ```python
    s = "Python syntax highlighting"
    print s
    ```

    ``` 
    No language indicated, so no syntax highlighting. 
    But let's throw in a <b>tag</b>.
    ```
```

inline `code`

```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```
 
```python
s = "Python syntax highlighting"
print s
```

``` 
No language indicated, so no syntax highlighting. 
But let's throw in a <b>tag</b>.
```

## <span style="color:seagreen">Table</span>
------

Colons can be used to align columns.

``` markdown
| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

There must be at least 3 dashes separating each header cell.
The outer pipes (|) are optional, and you don't need to make the 
raw Markdown line up prettily. You can also use inline Markdown.

Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3
```

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

There must be at least 3 dashes separating each header cell.
The outer pipes (|) are optional, and you don't need to make the 
raw Markdown line up prettily. You can also use inline Markdown.

Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3

## <span style="color:seagreen">Blockquote</span>
------
```markdown
> Blockquotes are very handy in email to emulate reply text.
> This line is part of the same quote.

Quote break.

> This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can *put* **Markdown** into a blockquote. 
```

> Blockquotes are very handy in email to emulate reply text.
> This line is part of the same quote.

Quote break.

> This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can *put* **Markdown** into a blockquote. 

## <span style="color:seagreen">Inline HTML</span>
------

``` markdown
<dl>
  <dt>Definition list</dt>
  <dd>Is something people use sometimes.</dd>

  <dt>Markdown in HTML</dt>
  <dd>Does *not* work **very** well. Use HTML <em>tags</em>.</dd>
</dl>
```

<dl>
  <dt>Definition list</dt>
  <dd>Is something people use sometimes.</dd>

  <dt>Markdown in HTML</dt>
  <dd>Does *not* work **very** well. Use HTML <em>tags</em>.</dd>
</dl>

## <span style="color:seagreen">Horizontal Rule</span>
------

``` markdown
Three or more...
---

Hyphens
***

Asterisks
___

Underscores
```

Three or more...

---
Hyphens

***
Asterisks

___
Underscores

## <span style="color:seagreen">Line Breaks</span>
------

```markdown
Here's a line for us to start with.

This line is separated from the one above by two newlines, so it will be a *separate paragraph*.

```

Here's a line for us to start with.

This line is separated from the one above by two newlines, so it will be a *separate paragraph*.

