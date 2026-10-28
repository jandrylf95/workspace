# Markdown Syntax


## 1. Headings
`# Heading 1 (maps to <h1>)`
# H1
`## Heading 2 (maps to <h2>)`
## H2
`### Heading 3 (maps to <h3>)`
### H3
`#### Heading 4 (maps to <h4>)`
#### H4
`##### Heading 5 (maps to <h5>)`
##### H5
`###### Heading 6 (maps to <h6>)` 
###### H6


## 2. Text Formatting & Styling

`**Bold text** or __Bold text__` **Bold text**

`*Italic text* or _Italic text_` *Italic text*

`***Bold and italic*** or ___Bold and italic___` ***Bold and italic***

`~~Strikethrough~~ (GFM extension)` ~~Strikethrough~~

```
Subscript: H~2~O (Supported in extended GFM parsers)
Superscript: X^2^ (Supported in extended GFM parsers)
==Highlighted text== (Supported in extended markdown engines)
```


## 3. Paragraphs, Breaks & Dividers
First paragraph text.

Second paragraph (separated by a blank line).

Line break inside a paragraph: end the line with two spaces  
or use a backslash at the end of the line\
to force a `<br>` break.

Ex: jkflskdjlfskdjlskdfjlskdfjlsd  kjslkjdlskjdlas 


Horizontal rule / thematic break (three or more `-`, `*`, or `_`)
***
---
___


## 4. Blockquotes

> Single-level blockquote.
>
> Multi-line blockquote with an internal paragraph.

>> Nested blockquote (level 2).
>>> Nested blockquote (level 3).

> **Admonition / Callout (GitHub extension):**
> [!NOTE]
> Useful information that users should know.

> [!WARNING]
> Critical alerts regarding system or data integrity.


## 5. Lists

<!-- Unordered Lists -->
* Item 1
* Item 2
  * Nested item (indent 2 or 4 spaces)
  * Another nested item
- Item 3
+ Item 4

<!-- Ordered Lists (Numbers auto-increment in HTML) -->
1. First step
2. Second step
3. Third step
   1. Sub-step A
   2. Sub-step B

<!-- GFM Task Lists / Checklists -->
- [x] Completed task
- [ ] Incomplete pending task
- [ ] Another pending task


## 6. Code Spans and Fenced Code Blocks

Inline code: Use `const connection = new PDO(...)` inside running text.

Fenced code block without highlighting:
```
git status
git pull origin main
```

Fenced code block with declarative language syntax highlighting:
```sql
SELECT user_id, email, status 
FROM app_users 
WHERE status = 'ACTIVE' 
LIMIT 10;
```

```php
<?php
declare(strict_types=1);

function get_cluster_status(string $clusterId): array {
    return ['id' => $clusterId, 'healthy' => true];
}
```

## 7. Link and Images

<!-- Standard Hyperlink -->
[Visit UTPL](https://www.utpl.edu.ec)

<!-- Link with Hover Title -->
[GitHub Docs](https://docs.github.com "Official Documentation")

<!-- Reference-Style Link -->
[Database Reference][1]

[1]: https://dev.mysql.com/doc/ "MySQL Manual"

<!-- Automatic URL Linking (Autolinks) -->
<https://github.com>
<developer@example.com>

<!-- Images -->
**Image Alt Text**
![Image Alt Text](https://upload.wikimedia.org/wikipedia/commons/c/c4/Evil_pixel_art_face_%28300x300%29.png?utm_source=commons.wikimedia.org&utm_campaign=index&utm_content=original)
**Image with Hover Title**
![Image with Hover Title](https://upload.wikimedia.org/wikipedia/commons/c/c4/Evil_pixel_art_face_%28300x300%29.png?utm_source=commons.wikimedia.org&utm_campaign=index&utm_content=original "Architecture Schema")

**Clickable Image Alt** <!-- Linked Image (Clickable diagram) -->
[![Clickable Image Alt](https://upload.wikimedia.org/wikipedia/commons/c/c4/Evil_pixel_art_face_%28300x300%29.png?utm_source=commons.wikimedia.org&utm_campaign=index&utm_content=original)](https://upload.wikimedia.org/wikipedia/commons/c/c4/Evil_pixel_art_face_%28300x300%29.png?utm_source=commons.wikimedia.org&utm_campaign=index&utm_content=original)

## 8. Tables (GFM Syntax)

| Left-Aligned | Center-Aligned | Right-Aligned | Columna adicional |
| :--- | :---: | ---: | :---: |
| Text string | Token / Flag | Integer / Value |
| `localhost` | `3306` | $450.00 |
| `db.internal` | `6379` | $1,280.50 |
| --- | --- | --- | `<h1>` |

## Escaping Characters

\*This text will not be italicized\*
\# This is not a heading
\[This is not a link\]