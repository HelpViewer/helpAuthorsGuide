# 🖨️ Print

## 🖼️ Icons

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

## Collapsible section

All collapsible sections are automatically opened before printing to ensure that all text is printed.

## 📄 Page break for printing

To manually insert a page break, add the following line to your .md or .html file:

```markdown
<!-- @print-break -->
```

⚠️ Note: Make sure to type the text exactly as shown, including spaces.

When generating the print version, the document will automatically break at this point, and the following content will start on a new page.
