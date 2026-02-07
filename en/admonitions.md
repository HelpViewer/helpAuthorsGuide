# 📢 Highlighted information blocks (admonitions)

The implementation of marked information blocks is based on the admonitions style commonly used in documentation (e.g., GitHub Docs) and is designed to be compatible with this style. This part of the application can be removed by the administrator during installation - in this case, the syntax will still be valid, but the blocks will only be displayed as a normal, left-aligned paragraph (blockquote).

- The notation is **> [!TYPE]Information text.**
- The following types are defined: NOTE, TIP, IMPORTANT, WARNING, CAUTION. Any other type is marked only with a silver line
- Links within the text of the information must be included with the target path within this block (links to the footer of the page are not allowed - see example below)

```markdown
> [!NOTE]**Note**
Description on the next line.  
Description on the third line.

> [!TIP]Tip for readers
> [!IMPORTANT]This point is important.
Important notice for ```<script>``` blocks can be found on the [example](innerJS.md "Example") page. 

> [!WARNING]Warning: yellow exclamation mark!

> [!CAUTION]Warning: red exclamation mark!

> [!MYTEST]Block of unknown type
```

Example:

> [!NOTE]**Note**
Description on the next line.  
Description on the third line.

> [!TIP]Tip for readers
> [!IMPORTANT]This point is important.
Important note for ```<script>``` blocks can be found on the [example](innerJS.md "Example") page. 

> [!WARNING]Warning: yellow exclamation mark!

> [!CAUTION]Warning: red exclamation mark!

> [!MYTEST]Block of unknown type

Chapter 🏷️ [Branding][Branding] describes the options for customizing the appearance of these blocks, including defining your own block type.

[Branding]: branding.md#h-3-8 "🏷️ Branding"
