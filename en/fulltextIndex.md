# 🔎 Fulltext search (fts-keywords.lst)

- File is used for fulltext search (🔎)
- It is located in language version subdir.
- Each language has its own independent copy.
- If file **exists, then it is turned on** the creation of fulltext index during publishing process. There are no more steps needed from side of help author.
- Keep file empty
- If you want to turn off the fulltext index, then delete this file.

## Logic description in general

In repository [fulltextSearchDBBuilder][FTSIndexing] there is stored all logic of fulltext index assembly process. It is bash script.

For each one language independently there will be done these steps:

1. Select files: \*.md;\*.htm;\*.html for indexing
2. All content is converted to UTF-8 code page
3. Missing files in [file list][Dfiles.lst] are attached to end of list without any backup heading
4. All letters are converted to lowercase
5. Letters are stripped of diacritics and special characters (e.g.: about:blank -> aboutblank)
6. Words smaller than 3 letters are excluded from next processing
7. There is counted sum of emerges of words in each of indexed document/chapter
8. The documents are ordered by word count from highest to lowest for each word
9. Two new files will be created:
    - fts-keywords.lst (words)
    - fts-keywords-files.lst (word to files interconnection list)  
  Files follow the same structure as defined in [keywords][Dkeywords.lst]

[FTSIndexing]: https://github.com/HelpViewer/fulltextSearchDBBuilder "Fulltext index assembly"
[Dkeywords.lst]: mdata/keywords.lst.md "keywords.lst"
[Dfiles.lst]: mdata/files.lst.md "files.lst"
