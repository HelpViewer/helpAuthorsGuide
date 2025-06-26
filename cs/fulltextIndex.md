# 🔎 Fulltextové vyhledávání (fts-keywords.lst)

- Soubor je využíván v případě  fulltext vyhledávání (🔎)
- Nachází se v jazykové verzi nápovědy.
- Každý jazyk má svoji kopii.
- Pokud soubor **existuje, je zapnuto** vytvoření fulltext indexu při vydávání nápovědy. Dalšího zásahu ze strany autora zde není potřeba.
- Soubor ponechte prázdný
- Pro vypnutí vytvoření fulltext indexu stačí soubor z jazykové verze smazat.

## Obecný popis logiky

Logika procesu přípravy fulltext indexu se nachází v repozitáři [fulltextSearchDBBuilder][FTSIndexing] (jedná se o bash skript)

Pro každý jazyk samostatně proběhnou tyto kroky:

1. Do indexace se vyberou soubory: \*.md;\*.htm;\*.html
2. Vše se převede na UTF-8 kódovou stránku
3. Chybějící soubory v [seznamu souborů][Dfiles.lst] jsou vloženy na konec seznamu bez záložního nadpisu
4. Všechna písmena textu se převedou na malá
5. Odebere se diakritika a speciální znaky (about:blank -> aboutblank)
6. Slova s délkou menší než 3 písmena jsou vynechána ze zpracování
7. Spočítá se počet výskytů unikátních slov v jednotlivých dokumentech
8. Dokumenty se seřadí od největšího k nejmenšímu počtu výskytu v seznamech pro jednotlivá slova
9. Sestaví se dva nové soubory:
    - fts-keywords.lst (slova)
    - fts-keywords-files.lst (propojené soubory)  
  Soubory jsou strukturou stejné se seznamem [klíčových slov][Dkeywords.lst]

[FTSIndexing]: https://github.com/HelpViewer/fulltextSearchDBBuilder "Sestavení fulltext indexu"
[Dkeywords.lst]: mdata/keywords.lst.md "keywords.lst"
[Dfiles.lst]: mdata/files.lst.md "files.lst"
