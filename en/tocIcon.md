# 📖 TOC icons

TOC icons are determined from data of selected language version in this order (from most significant):

| Icons | Source |
|---|---|
| (image) | In language version there exists: **book-open.png** and **book-closed.png** |
| <ul class="tree" id="tree"><details><summary></summary></details></ul> | **_config.txt** contains keys  **OverrideBookIcon-opened**, **OverrideBookIcon-closed** with filled values (unicode character, letter, text; path is not allowed to be here) |
| <details><summary></summary></details> | Not anything from upper options has been valid |

If any of the rules in the table above are met, the other rules are no longer taken into account.

## Subitem icons

| Icons | Source |
|---|---|
| (image) | In language version there exists: **tree-sibling.png** |
| (icon) | **_config.txt** contains the key **OverrideBookIcon-sibling** with a non-empty value (unicode character, letter, text; path is not allowed to be here) |
| (nothing) | Not anything from upper options has been valid |

If any of the rules in the table above are met, the other rules are no longer taken into account.
