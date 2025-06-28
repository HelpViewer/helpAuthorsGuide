# 🌐 New language for help file

1. For a new help language, you need to create a new directory with the language abbreviation in your main level repository.
    - To determine this abbreviation, refer to the list of known language abbreviations in the [localization Repository][Localiz] HelpViewer. This has the advantage of automatically switching the user's version of help when setting the language of the entire environment.
    - If no suitable abbreviation exists, choose an abbreviation ideally according to **ISO 639-1**. 
    - You can write help in your language, even if **HelpViewer** itself is not localized.
2. The directory should ideally be based on a copy of an existing localization that you understand, so that you have the texts of both languages side by side.
3. Do not change file names or locations.
4. Translate the indexing files:
    - 📑 [files.lst][Dfiles.lst] - right half (backup headings)
    - 📇 [keywords.lst][Dkeywords.lst] - list of keywords
    - 📖 [tree.lst][Dtree.lst] - topic tree
5. Translate the texts of the chapters.
6. The names of the bookmarks (anchors) will be changed as the chapters are translated (make sure the links are valid).

[Localiz]: https://github.com/HelpViewer/Translations "HelpViewer localization"
[Dfiles.lst]: mdata/files.lst.md "files.lst"
[Dkeywords.lst]: mdata/keywords.lst.md "keywords.lst"
[Dtree.lst]: mdata/tree.lst.md "tree.lst"
