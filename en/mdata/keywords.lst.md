# 📇 Keywords list (keywords.lst)

- ⚠️ This format is very strict, please follow the rules exactly.
- Defines keywords list in help
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
| [1] | Keyword |
| [2] | Optional. Synonym for a given word. If it should be used, then If it is to be used, it is always preceded by a semicolon (**;**) and may be repeated any number of times. |

## Rules

- A space is not a word separator
- A line never ends with a semicolon
- At least position [1] must be defined
- Synonyms are broken down into individual words and the user is offered the same list of topics for all these words (**keywords-files.lst**)
- If synonyms overlap across rows (one synonym appears on multiple rows), HelpViewer will build a merged list of topics in which each topic will only appear once (decided here by files.lst)
