# 🧩 Vložený JavaScript

Do **md** textu je možno vložit JavaScript blok, který se vykoná po načtení stránky.

Obsah kapitoly se načte, zobrazí se a s krátkým odstupem se provedou potřebné funkce inline javascriptu.

💡 Doporučení:
- Buďte, prosím, slušní a využívejte tuto funkci aplikace uvážlivě s ohledem na uživatelský komfort a dodržení pravidel přístupnosti u své nápovědy. HelpViewer zde žádným způsobem nezasahuje do logiky skriptu, pouze ji předá k dalšímu zpracování na straně klienta.  
  **Za obsah a dopady skriptů vložených v rámci nápovědy nese odpovědnost autor nápovědy.**

> [!WARNING] Administrátor systému má možnost volitelně nainstalovat aplikaci s:  
  
- vypnutím funkce 🧾 Vykonávat vložený JavaScript
- aktivní funkcí 📦🛡️ DOMPurify.  
  
V takovémto případě by tato část aplikace byla nefunkční.  
Důvodem pro existenci těchto funkcí v systému je ochrana proti XSS útoku.  
Funkce jsou **ve výchozím nastavení** v instalaci **zahrnuty** (tedy javascript nebude možno spouštět - DOMPurify musí být vypnuta).

```markdown
1. Stáhněte si balíček <span id="linkhereI"></span> a rozbalte jej.

<script>
  insertDownloadLink('linkhereI');
</script>
```

U funkce insertDownloadLink můžete také provést volání insertDownloadLink('cilovy prvek', 'maska'), kde v textu masky bude speciální znak:

- @ = nejnovější verze
- | = package.zip (stejné chování jako bez masky)
- _ = současná verze aplikace HelpViewer (nikoli nápovědy) u uživatele

Ukázka připraví hypertextový odkaz na stažení poslední vydané verze **HelpViewer** a vloží jej do pojmenovaného prvku span:

1. Stáhněte si balíček <span id="linkhereI"></span> a rozbalte jej.

<script>
  insertDownloadLink('linkhereI');
</script>
