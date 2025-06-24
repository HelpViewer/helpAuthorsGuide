# 🌐Nový jazyk nápovědy

1. Pro nový jazyk nápovědy je potřeba ve Vašem repozitáři na hlavní úrovni založit nový adresář se zkratkou jazyka.
    - Při určení této zkratky se řiďte seznamem zkratek známých jazyků v [repozitáři lokalizací][Localiz] HelpViewer. Výhodou tohoto postupu je automatické přepnutí verze nápovědy uživatelem při nastavení jazyka celého prostředí.
    - Pokud neexistuje vhodná zkratka, zvolte zkratku ideálně podle standardu **ISO 639-1**. 
    - Nápovědu můžete psát ve svém jazyce, i když samotný **HelpViewer** není lokalizovaný.
2. Adresář založte ideálně kopií existující lokalizace, které rozumíte, abyste texty obou jazyků měl vedle sebe.
3. Jména souborů ani umístění neměňte.
4. Přeložte indexační soubory:
    - 📑 [files.lst][Dfiles.lst] - pravou polovinu (záložní nadpisy)
    - 📇 [keywords.lst][Dkeywords.lst] - seznam klíčových slov
    - 📖 [tree.lst][Dtree.lst] - strom témat
5. Přeložte texty kapitol.
6. Jména záložek (kotev) budou změněna s přeložením kapitol (ujistěte se o platnosti odkazů).

[Localiz]: https://github.com/HelpViewer/Translations "Lokalizace HelpViewer"
[Dfiles.lst]: mdata/files.lst.md "files.lst"
[Dkeywords.lst]: mdata/keywords.lst.md "keywords.lst"
[Dtree.lst]: mdata/tree.lst.md "tree.lst"
