# 📝 Chapter text

HelpViewer predicts all texts will be coded in **UTF-8 no BOM (65001)** code page.

In chapter text you can use all the standard syntax of **[md][MDSyntax]** document as e.g. **#** tag for heading even to lovel 6 (e.g. **###### Heading**).

You can also intersperse the md code with html or javascript code if needed.

In next subchapters of this chapter there are more information which you should know and also HelpViewer features you can use.

## 🔖 Sections List

**HelpViewer** automatically assembles a list of sections (🔖) based on the document's headings (h1-h6, i.e. # ... ######), providing users with a quick and convenient way to navigate through the chapter.

- If the document contains only a main heading (h1 / #), the list will not be shown.
- The list becomes available as soon as there is at least one additional heading of any level (h1-h6).

Headings are automatically named in the following format: #h-(level)-(order).
  - level is a number from 1 to 6 indicating the heading level (h1 = 1, ..., h6 = 6)
  - order is a zero-based index that reflects the heading’s position among headings of the same level across the entire chapter.

Determining the order:
- Each heading level has its own counter (h1, h2, ..., h6 are tracked separately).
- Headings are indexed in the order they appear - left to right, top to bottom.
- ⚠ If a new heading is inserted between two existing ones, it inherits the index of the heading that originally occupied that position. All subsequent headings at the same level are automatically shifted.

This ensures that anchors remain consistent and predictable, even as the document structure evolves.

## 🖼️ Icons

Inside chapter text you can insert unicode letters/characters also. Some of them stands for icons which you can use without need to install any other external library.

The insertion into the chapter text is done either by direct copy of the character or by inserting two other formats (HTML character entities):
```markdown
💡
&amp;#128161;
&amp;#x1F4A1;
```

For exact codes and situations I advice to use Copilot/ChatGPT, which will help you find suitable icons quickly.

### Icons and printing

Icons are automatically removed from the text before printing. If you are not comfortable with this behavior, you can modify it either at the configuration level of the entire help or by using a directive in a specific topic.

If you want to keep the icons in a specific topic, insert this directive after the first chapter heading (it must not be before the heading) or later in the topic text:

```markdown
# &#128214;Help Viewer overview

<!-- @print-keep-icons -->
The application is divided into two main areas:
```

⚠️ Note: Type the directive with the exact spacing as shown and do not combine it with other comments or blocks. This will ensure correct processing and no problems.

To keep the icons in all topics, set the help configuration option **OverridePrintKeepIcons** to 1.

For a more detailed description of the behavior:

| OverridePrintKeepIcons | print-keep-icons | Result |
|---|---|---|
| 0 / not | not | icons removed |
| 1 | not | icons retained |
| 0 | present | icons retained |
| 1 | present | icons removed |

## Lists

For correct bullet list item there is required to have a space between marking (number for numbered list, - for bullet list):

```markdown
- Point2
1. Point2
```

Example (pair - wrong and right):

A)

-Point1
- Point2

B)

1.Point1
1. Point2

## Paragraphs

In case of paragraph there is need to have one empty row between them in **md** file:
```markdown
First paragraph

Second paragraph
```

Example:

First paragraph

Second paragraph

## Two spaces on the end of line

If you will use on the end of one line twice the space ( ) character and you will continue with another line afterwards then you will provide the same spacing for new line as the previous one line had:

```
  - ☰ Show left panel back__
    *(if hidden)*
```
In this code listing there underscores (_; 2 are here) stands for spaces ( ) to be clearly visible.

Example:

  - ☰ Show left panel back  
    *(if hidden)*

## Collapsible section

With usage of plain HTML code you can create collapsible section in text of your chapter. Rendering logic will correctly transfers to correct output for user.

```html
<details>
<summary>There is main heading here. Another information will be shown when it will be clicked</summary>
There is extended description of given point.
</details>
```

Example:
<details>
<summary>There is main heading here. Another information will be shown when it will be clicked</summary>
There is extended description of given point.
</details>

[MDSyntax]: https://www.markdownguide.org/basic-syntax/ "MD syntax"
