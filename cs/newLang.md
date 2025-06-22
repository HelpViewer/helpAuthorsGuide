# 🌐Nový jazyk nápovědy

1. Pro nový jazyk nápovědy je potřeba ve Vašem repozitáři na hlavní úrovni založit nový adresář se zkratkou jazyka.
    - Při určení této zkratky se řiďte seznamem zkratek známých jazyků v [repozitáři lokalizací][Localiz] HelpViewer. Výhodou tohoto postupu je automatické přepnutí verze nápovědy uživatelem při nastavení jazyka celého prostředí.
    - Pokud neexistuje vhodná zkratka, zvolte zkratku ideálně podle standardu **ISO 639-1**.
2. Adresář založte ideálně kopií existující lokalizace, které rozumíte, abyste texty obou jazyků měl vedle sebe
3. Jména souborů neměňte.
4. Přeložte indexační soubory:
    - 📑 files.lst - pravou polovinu (záložní nadpisy)
    - 📇 keywords.lst - seznam klíčových slov
    - 📖 tree.lst - strom témat

[Localiz]: https://github.com/HelpViewer/Translations "Lokalizace HelpViewer"