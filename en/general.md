# 💡 General recommendation and information sources

In GitHub organization **[HelpVewer][HV]** you will find repositories starting with **help\***. With exception of **helpTemplate** and **HelpViewer** all of them are examples of help files. You can take any **Release** of these and its all attachments named like this mask **Help-*.zip**. Archives are passwordless so its content is accessible to browsing.

During your help file creation you can browse it in offline even if it has not been released. This way you can verify future results and behavior. You can do it this way - start **HelpViewer** in web browser with browsing local file content and you will give it relative dir path to your new help file:
```
file://.../HelpViewer/?d=../yourhelp/__/
```

- __ stands for short code of selected language by user.
- If path doesn't works, then replace slashes **/** in d parameter for **%2F**
- Fulltext search will not work here (index is being built just during releasing of help file)

Phrase **[pub]** in commit text message is important - runs release of your help file. Prepare in this commit update of your CHANGELOG.md file for contain new version description on start of the file. It will be automatically used for Release notes.

[HV]: https://github.com/orgs/HelpViewer/repositories "Repositories"
