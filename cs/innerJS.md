# 🧩 Vložený JavaScript

Do **md** textu je možno vložit JavaScript blok, který se vykoná po načtení stránky.

Obsah kapitoly se načte, zobrazí se a s krátkým odstupem se provedou potřebné funkce inline javascriptu.

💡 Doporučení:
- Buďte, prosím, slušní a využívejte tuto funkci aplikace uvážlivě s ohledem na uživatelský komfort a dodržení pravidel přístupnosti u své nápovědy. HelpViewer zde žádným způsobem nezasahuje do logiky skriptu, pouze ji předá k dalšímu zpracování na straně klienta.  
  **Za obsah a dopady skriptů vložených v rámci nápovědy nese odpovědnost autor nápovědy.**

```
1. Stáhněte si balíček &lt;span id="linkhereI"&gt;&lt;/span&gt; a rozbalte jej.

&lt;script&gt;
  async function insertDownloadLink() {
    const fname = 'package.zip';
    const path = await getLatestReleaseBundleUri(null, fname);
    const parentO = document.getElementById('linkhereI');
    parentO.innerHTML = `&lt;a href="${path}" alt="${fname}" title= "${path}"&gt;${fname}&lt;/a&gt;`;
  }

  insertDownloadLink();
&lt;/script&gt;
```

Ukázka připraví hypertextový odkaz na stažení poslední vydané verze **HelpViewer** a vloží jej do pojmenovaného prvku span:

1. Stáhněte si balíček <span id="linkhereI"></span> a rozbalte jej.

<script>
  async function insertDownloadLink() {
    const fname = 'package.zip';
    const path = await getLatestReleaseBundleUri(null, fname);
    const parentO = document.getElementById('linkhereI');
    parentO.innerHTML = `<a href="${path}" alt="${fname}" title= "${path}">${fname}</a>`;
  }

  insertDownloadLink();
</script>
