# 📇 Keyword - file connection (keywords-files.lst)

- ⚠️ This format is very strict, please follow the rules exactly.
- This file defines interconnection of keywords ([keywords.lst][Dkeywords.lst]) and file list ([files.lst][Dfiles.lst])
- One row = one item
- Line break in the uncomplete definition is not allowed
- This file is used for the keywords dictionary (📇)

## File structure

```
[1]
[1];[2]
```

## Position description

| Position | Description |
|---|---|
| [1] | Zero based index of interconnected file |
| [2] | Zero based index of interconnected file. Repeating of this information is allowed, but just before this semicolon (**;**) is required. |

## Rules

- A line never ends with a semicolon
- Semicolon is the delimiter for any single interconnection definition
- Each line in this file corresponds to the same line in the keyword file. If you open the two files side by side, you can think of them as two columns of a table - the corresponding information is on the same rows.

[Dfiles.lst]: mdata/files.lst.md "files.lst"
[Dkeywords.lst]: mdata/keywords.lst.md "keywords.lst"
