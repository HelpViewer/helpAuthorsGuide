# 📥 Export

Tlačítko 📥 Export (napravo na horním panelu nad textem kapitoly) Vám po kliknutí nabídne export textu kapitoly do několika formátů.

## Formáty

- **HTM**  
  Jedna [HTML][HTML5Syntax] stránka s veškerým obsahem kapitol (princip jednotné knihy)
- **MD**  
  [markdown][MDSyntax] zdrojový kód
- **TEX**  
  [LaTeX][LATEX] zdrojový kód pro následný výstup do **PDF**
- **EPUB**  
  ePub e-book formát kompatibilní s verzí ePub2 a ePub3  
  (otestováno primárně na SW čtečkách - [EPUBReader][EPUBReader] (Chrome), dále na Android - [ReadEra][readera], [eBoox][eboox])  
  Pokud není k dispozici seznam témat, exportní modul se jej pokusí vytvořit z **h1** nadpisů v kapitolách.
- **RTF**  
  - Zdrojový kód je kompatibilní s **Word 97 (RTF 1.5)** a vyšší.
  - Formát textu je pouze v základním rozsahu (i když váš HTML může mít složitější formát - zejména podbarvení a barvy textu nejsou při exportu řešeny).
  - Nadpisy jsou správně definovány, ale bez speciálního formátu (ve Wordu můžete styl šablony snadno změnit).
  - Výstup z **Prism** se tiskne písmem typu "psací stroj" (bez barev a formátu).
  - Výstup z **Marked** se neexportuje.
  - Používá výchozí **kódovou stránku ANSI** (při exportu jazyků východní Evropy a dalších mohou být znaky s diakritikou poškozené).
  - Obrázky nejsou exportovány.
  - Tabulky jsou exportovány jen jako text s tabulátory.
  - Unicode znaky jsou poškozené, ale vložené (jako více prostých ASCII znaků).
- **STATIC**  
  Sada HTML stránek, které jsou:
  - statické,
  - minifikované,
  - propojené mezi sebou relativními URI cestami,
  - doplněné o SEO metadata (og*:, description),
  - CSS styly a HTML struktura jsou stále kompatibilní s **HelpViewer** (znovuvyužitelné vlastní styly pro HelpViewer bez nutnosti dalších úprav),
  - UI prvky jsou redukovány na základní hypertextové odkazy (ikony jsou převzaty z tlačítek v době exportu),
  - inspirovány principy standardu přístupnosti WCAG 2.1 AA,
  - 💬 Texty a tooltipy na tlačítcích a dalších prvcích jsou převzaty z aktivní lokalizace v době exportu,
  - neobsahují JavaScript z aplikační logiky **HelpViewer** a nepotřebují aplikaci ke svému běhu,  
    JavaScript z kapitol nápovědy, který autor do textu vložil je zahrnut.  
    JavaScript odkazovaný v head sekci zahrnut není.
  - CSS styly externích komponent (Mermaid, Prism) jsou převzaty, JavaScript je vynechán.
  - Pokud není k dispozici seznam témat, exportní modul se jej pokusí vytvořit z prvních **h1** nadpisů jednotlivých kapitol.
  - Volitelně je možné zahrnout i export seznamu 📇 [klíčových slov][Dkeywords.lst] nebo seznamu pro 🔎 [fulltextové vyhledávání][fulltextIndex]
  - Omezení exportu:
    - ✨ **Úvodní obrazovka**, 💧 **Vodoznak** nejsou součástí exportu.
    - 🌐 Jazyky - exportována je pouze aktivní jazyková verze. Přepínání mezi jazyky nebude možné.
  - Podpora vlastních úprav:
    - Prázdný soubor **src/custom.css** Vám dovoluje doplnit si další potřebné úpravy CSS stylu po exportu.
    - V souborech **sitemap.xml** a **robots.txt** nahraďte **\_REMOTEHOST\_** úplnou URI Vaší cílové domény kam budete stránky nasazovat.

## Omezení

- Exporty vždy pracují pouze s viditelným textem kapitoly. Vyjímkou jsou seznamy u **STATIC** exportu.
- Administrátor může nainstalovat aplikaci bez některých exportních formátů.
- Administrátor může funkci zcela odebrat z instalace - tlačítko pak chybí.

## Součinnosti

- V kombinaci s funkcí 📚 Zobrazit všechny kapitoly jako **jeden dokument** (administrátor může odebrat z instalace také) můžete exportovat celou dokumentaci.  
  Kde je to vhodné, tak proces exportu využívá zde zvolené konfigurační volby.  
  Funkce se doplňují, ale nemusí být v aplikaci nainstalovány obě.  
  Volba **Static: Exportovat slovníky** rozhoduje, zda budou exportovány i seznamy klíčových slov a fulltextu (export s nimi je výrazně větší).
- V kombinaci s funkcí 🖨️ **Vytisknout** je možné z textu kapitol odebrat [unicode ikonky][IconPrint] tímto postupem:
  1. Ve funkci **jeden dokument** vyberte v **Tisk ikonek** volbu **Odebrat**
  2. Kliknutím na **Vytisknout** si zobrazte náhled před tiskem, který zrušte (neodesílejte na tiskárnu)
  3. Ikonky  budou odebrány a exporty pracují s viditelným textem kapitoly.
- Funkce 🖨️ **Vytisknout** běžně dovoluje v moderních prohlížečích tisk stránky do **PDF**
- V kombinaci s funkcí [👀 Zobraz repozitář][viewRepo] lze číst volně dostupné externí zdroje (například volnou sadu propojených md souborů)
- S použitím parametru **d** v URI ([index.html?d=index.html?d=https://helpviewer.github.io/][test]) lze číst volně dostupné externí zdroje

[MDSyntax]: https://www.markdownguide.org/basic-syntax/ "MD"
[HTML5Syntax]: https://www.tutorialspoint.com/html5/html5_syntax.htm "HTML"
[LATEX]: https://www.latex-project.org/ "LaTeX"
[EPUBReader]: https://chromewebstore.google.com/detail/epubreader/jhhclmfgfllimlhabjkgkeebkbiadflb "EPUBReader"
[readera]: https://play.google.com/store/apps/details?id=org.readera "ReadEra"
[eboox]: https://play.google.com/store/apps/details?id=com.reader.books "eBoox"
[Dkeywords.lst]: mdata/keywords.lst.md "📇 Seznam klíčových slov (keywords.lst)"
[fulltextIndex]: fulltextIndex.md "🔎 Fulltextové vyhledávání (fts-keywords.lst)"
[viewRepo]: :viewRepo.htm "👀 Podívejte se na svůj repozitář"
[test]: ?d=https://helpviewer.github.io/
[IconPrint]: texts.md#h-2-0 "Unicode ikonky"
