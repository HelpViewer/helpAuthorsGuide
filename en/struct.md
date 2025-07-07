# 🗂️ Help project structure

## Directories

In repository you will see this structure:
```treeview
.github/
    workflows/
cs/
en/
```

## Structure

Meaning of these is:

| File / path | Meaning |
|---|---|
| .github/workflows/publish.yml | CI script, which does [help file build][build]. Results of it is Release with these attachments:  **Help-(language short code).zip** a **Help-.zip** with data of directory **_base** |
| README.md | Base project description (update according to your needs) |
| LICENSE | License text (update according to your needs) |
| CHANGELOG.md | Change log document. This file is a source for change notes attached to releases which you will publish |
| _base | Usually it is not defined or exists. You can overwrite [HelpViewer UI][cusui] here |
| _invariant | Shared data over all language version of help. During publishing when there is equality in file names in language version, the _invariant file will overwrite that equally named file in language directory. |
| directories cs, en, ... | 🌐 [Language version][newLang] of help file. When you will create new directory herem then you have created new language of your help. |

## Language version files

Subdirectory en/ :

| File / path | Meaning |
|---|---|
| _config.txt | [Help file configuration][configDesc] |
| files.lst | [File list][Dfiles.lst] with relative paths and heading for dictionaries/lists and backup headings to chapters. |
| fts-keywords.lst | 🔎 If this file exists, then publishing process will prepare also [fulltext index][Dfts-keywords.lst]. If you will delete this file, then you will deactivate this feature. Keep file empty in content. |
| keywords.lst | 📇 [Keywords and synonyms][Dkeywords.lst] list. You have to fill this file manually. In case this file will not exists or it will be empty, then this feature will be deactivated. |
| keywords-files.lst | Relation between [keywords and files][Dkeywords-files.lst] |
| tree.lst | 📖 Definition of table of contents ([TOC][Dtree.lst]). In case this file will not exists or it will be empty, then this feature will be deactivated. |
| README.md | 🏡 Help main page. It will be automatically opened as first. Button on left bottom panel is directly pointing to this page. |

- In language subdir you can freely create new subdirs as you want. 
- Hyperlinks between chapters keep in relative paths between source and target file.

[Dfiles.lst]: mdata/files.lst.md "files.lst"
[Dkeywords.lst]: mdata/keywords.lst.md "keywords.lst"
[Dtree.lst]: mdata/tree.lst.md "tree.lst"
[Dfts-keywords.lst]: fulltextIndex.md "fts-keywords.lst"
[configDesc]: helpCfg.md ""
[Dkeywords-files.lst]: mdata/keywords-files.lst.md "keywords-files.lst"
[newLang]: newLang.md ""
[build]: publish.md ""
[cusui]: customUI.md "UI customization"
