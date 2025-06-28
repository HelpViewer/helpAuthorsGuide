# 🧩 Inline JavaScript

Into **md** text you can insert JavaScript code block, which will be executed after chapter text is loaded.

Chapter text is loaded and sfter that with short time delay there will be executed functions of inline JavaScript.

💡 Recommendation:
- Please be courteous and use this feature of the app judiciously with respect to user experience and adherence to accessibility rules for your help. HelpViewer does not interfere with the script logic here in any way, it just passes it on to the client side for further processing.  
  **The author of the help is responsible for the content and effects of the scripts embedded within the help.**

```
1. Download &lt;span id="linkhereI"&gt;&lt;/span&gt; and unzip it.

&lt;script&gt;
  insertDownloadLink('linkhereI');
&lt;/script&gt;
```

With insertDownloadLink function you can do call insertDownloadLink('target object id', 'mask'), where in mask text will be any of these special characters:

- @ = newest version
- | = package.zip (as same behavior as without any mask specified)
- _ = current version of HelpViewer (not help file) user has currently opened

This example will prepare hyperlink to package with latest published version of **HelpViewer** and inserts it to named span object:

1. Download <span id="linkhereI"></span> and unzip it.

<script>
  insertDownloadLink('linkhereI');
</script>
