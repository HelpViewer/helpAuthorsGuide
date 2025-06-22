# 📊Diagram

Výpis diagramu do **md** vložíte tímto způsobem:

````
```mermaid
graph TD; 
  A-->B; 
  A-->C; 
  B-->D; 
  C-->D;
```
````

Ukázka:

```mermaid
graph TD; 
  A-->B; 
  A-->C; 
  B-->D; 
  C-->D;
```

- Pro další příklady a informace si přečtěte dokumentaci knihovny [Mermaid][Mermaid]. 
- V rámci přípravy balíčku HelpViewer je vždy použita v daný čas sestavení nejnovější verze Mermaid, která je publikována prostřednictvím [jsdelivr distribuce][MermaJsDelivr].

[Mermaid]: https://mermaid.js.org/intro/ "Mermaid - vykresluje grafy a schémata podle speciálních textových definic"
[MermaJsDelivr]: https://cdn.jsdelivr.net/npm/mermaid/dist/ "Mermaid - JsDelivr"
