# 🔗 Links in texts

- Two underscores (**__**) represents the selected language, which the system automatically adds from the user settings.
- Refer to documents in relative ways (using ..). 
- Use **forward - /** for slashes in path strings.
- For more complex links (going to another help), use **?** and enter only parameters to make the system transfer easier in the future

See below for common ways to define a link.

## Inside Help

### Other topic/page
```markdown
The file defines a link between [keywords][Dkeywords.lst] and a list of [files][Dfiles.lst]
// ... at the end of the file:
[Dfiles.lst]: mdata/files.lst.md "files.lst"
[Dkeywords.lst]: mdata/keywords.lst.md "keywords.lst"
```
The file defines a link between [keywords][Dkeywords.lst] and a list of [files][Dfiles.lst]

### Another topic and its subchapter
```markdown
Chapter [How the application works][working] discusses the basics of working with the application.
// ... at the end of the file:
[working]: README.md#how-it-works "How the application works"
```
*Here, the link created will automatically change with the language translation of the chapters.*

Chapter [How the application works][working] discusses the basics of working with the application.

## Outside the help file - URI path
```markdown
This solution also uses the [JSZip library][JSZIP].
// ... at the end of the file:
[JSZIP]: http://jszip.org/ "JSZip - support for ZIP files handling"
```
This solution also uses the [JSZip library][JSZIP].

<!-- @print-break -->

## Another help file

### Default page
```markdown
You will see [user documentation][userdoc] directly in the HelpViewer, just like you see this website now.
// ... at the end of the file:
[userdoc]: ?d=hlp-user/Help-__.zip "Help Viewer quick guide"
```

You will see [user documentation][userdoc] directly in the HelpViewer, just like you see this website now.

### Specific topic
```markdown
If the problem persists, go to [troubleshooting guide][trouble].
// ... at the end of the file:
[trouble]: ?d=hlp/Help-__.zip&p=trouble.md "Troubleshooting guide"
```

If the problem persists, go to [troubleshooting guide][trouble].

### URI from the network
```markdown
You will see [user documentation][userdoc2] directly in the HelpViewer, just like you see this website now.
// ... at the end of the file:
[userdoc2]: ?d=https://github.com/HelpViewer/helpUser/releases/download/20250615/Help-__.zip "Help Viewer quick guide"
```

You will see [user documentation][userdoc2] directly in the HelpViewer, just like you see this website now.

[Dfiles.lst]: mdata/files.lst.md "files.lst"
[Dkeywords.lst]: mdata/keywords.lst.md "keywords.lst"
[working]: README.md#how-it-works "How the application works"
[JSZIP]: http://jszip.org/ "JSZip - support for ZIP files handling"
[userdoc]: ?d=hlp-user/Help-__.zip "Help Viewer quick guide"
[trouble]: ?d=hlp/Help-__.zip&p=trouble.md "Troubleshooting guide"
[userdoc2]: ?d=https://github.com/HelpViewer/helpUser/releases/download/20250615/Help-__.zip "Help Viewer quick guide"
