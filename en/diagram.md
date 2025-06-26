# 📊 Diagram

You will insert diagram to **md** file this way:

````
```mermaid
graph TD; 
  A-->B; 
  A-->C; 
  B-->D; 
  C-->D;
```
````

Example:

```mermaid
graph TD; 
  A-->B; 
  A-->C; 
  B-->D; 
  C-->D;
```

- For more examples read the [Mermaid][Mermaid] library documentation. 
- During HelpViewer package praparation there is every time used the last one version of Mermaid, which is published in  [jsdelivr][MermaJsDelivr] distribution.

[Mermaid]: https://mermaid.js.org/intro/ "Mermaid library - renderer for diagrams defined by specific textual definitions"
[MermaJsDelivr]: https://cdn.jsdelivr.net/npm/mermaid/dist/ "Mermaid - JsDelivr"
