# Markdown Cheat Sheet

## Headings 

```md
# Heading 1 
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6
```

# Heading 1 
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6

---

## Horizontal Rule

```md
---
```

This is a horizontal rule.

---

It separates content.

---

## Text Formatting

```md
*italic text*
_more italic text_
```

*italic text*

_more italic text_

```md
**bold text**
__more bold text__
```

**bold text** 

__more bold text__

```md
**mix *and* match**
```

**mix *and* match**

```md
~~strikethrough text~~
```

~~strikethrough text~~

---

## Lists

```md
1. Item 1
2. Item 2
    1. Item 2a
    2. Item 2b

- Item 1
- Item 2
  - Item 2a
  - Item 2b
```

1. Item 1
2. Item 2
    1. Item 2a
    2. Item 2b

- Item 1
- Item 2
  - Item 2a
  - Item 2b

---

## Code Formatting

### Inline code

```md
Text inside `backtick` on a line will be formatted like code.
```

Text inside `backtick` on a line will be formatted like code.

### Fenced Code Blocks

<pre><code>```js
function sum (a, b) {
  return a + b;
}
```</code></pre>


```js
function sum (a, b) {
  return a + b;
}
```

--- 

## Blockquote

```md
> This is a blockquote
> 
> text1 
> > text2
```

> This is a blockquote
> 
> text1 
> > text2

---

## Links

To attach a link

```md
[YouTube](https://youtube.com "YouTube")
```

[YouTube](https://youtube.com "YouTube")

To attach a link using a reference

```md
[FB]: https://facebook.com "Facebook"

[Facebook][FB]
```

[FB]: https://facebook.com "Facebook"

[Facebook][FB]

To jump to the mentioned heading using the Heading ID

```md
[Blockquote](#blockquote)
```

[Blockquote](#blockquote)

---

## Images

```md
[![LINUX](https://www.linux.org/images/logo.png)](https://www.linux.org/)
```

[![LINUX](https://www.linux.org/images/logo.png)](https://www.linux.org/)

---

## Tables

Tables can be justified using ":".

```md
| Packages | Description          | Version   |
| :---     | :---:                | ---:      |
| **Left** | **Center**           | **Right** |
| React    | JavaScript Framework | v18.0     |
| Next.js  | React Framework      | v12.0     |
```

| Packages | Description          | Version   |
| :---     | :---:                | ---:      |
| **Left** | **Center**           | **Right** |
| React    | JavaScript Framework | v18.0     |
| Next.js  | React Framework      | v12.0     |

---

## Task List

```md
- [x] Task 1
- [x] Task 2
- [ ] Task 3
```

- [x] Task 1
- [x] Task 2
- [ ] Task 3

--- 

## Emojis 

```md
:smile: :tada:
```

:smile: :tada:

---

## Comments

To hide a comment
```md
[This is a hidden comment.]: #
```

[This is a hidden comment.]: #

---

## Toggle

```html
<details>
    <summary>This is a toggle !</summary>
    
    Contents of toggle.
</details>
```

<details>
    <summary>This is a toggle !</summary>
    
    Contents of toggle.
</details>

---

## Callouts

```md
> :bulb: **Tip:** Here's an important tip to remember!
```

> :bulb: **Tip:** Here's an important tip to remember!

---

For more info, please visit https://www.markdownguide.org/.