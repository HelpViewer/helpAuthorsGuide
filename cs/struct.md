# 🗂️Struktura projektu nápovědy

## Adresáře

V repozitáři se nachází tato adresářová struktura:
```
├───.github
│   └───workflows
├───cs
└───en
```

## Struktura repozitáře

Z pohledu souborů je význam následující:

| Soubor / cesta | Popis |
|---|---|
| .github/workflows/publish.yml | CI skript, který slouží pro [sestavení nápovědy][build]. Jeho výsledkem je vydání s přílohami **Help-(zkratka jazyka).zip** a **Help-.zip** s daty z adresáře **_base** |
| README.md | Základní popis projektu (upravte podle své potřeby) |
| LICENSE | Text licence (upravte podle své potřeby) |
| CHANGELOG.md | Záznam o změnách v projektu. Tento soubor slouží jako podklad pro popisy nových verzí, které vydáte |
| _base | Není standardně definován. V tomto adresáři můžete přepsat standardní UI prohlížeče |
| _invariant | Společná data pro všechny jazykové verze. Jejich obsah přepíše veškeré soubory se stejným jménem v jednotlivých jazykových složkách |
| adresáře cs, en, ... | 🌐 [Jazykové verze][newLang] nápovědy. Vytvořením nového adresáře založíte novou jazykovou verzi nápovědy. |

## Soubory jazykové verze

Podadresář cs/ :

| Soubor / cesta | Popis |
|---|---|
| _config.txt | [Konfigurace nápovědy][configDesc] |
| files.lst | [Seznam souborů][Dfiles.lst] s relativními cestami a nadpisů do rejstříků a záložních nadpisů kapitol |
| fts-keywords.lst | 🔎 Pokud existuje, sestavení nápovědy vygeneruje také [fulltext index][Dfts-keywords.lst]. Jeho smazáním tuto funkci deaktivujete. Soubor ponechte prázdný. |
| keywords.lst | 📇 Seznam [klíčových slov][Dkeywords.lst] a synonym. Musíte definovat ručně. V případě, že soubor nebude existovat nebo bude prázdný tuto funkci deaktivujete |
| keywords-files.lst | Vazba mezi [klíčovými slovy a soubory][Dkeywords-files.lst] |
| tree.lst | 📖 Definice [stromu témat][Dtree.lst]. V případě, že soubor nebude existovat nebo bude prázdný tuto funkci deaktivujete |
| README.md | 🏡 Hlavní stránka nápovědy. Otevře se automaticky jako první. Tlačítko na spodním panelu na ni přímo odkazuje |

- V podsložce můžete zakládat další podsložky podle své potřeby. 
- Odkazy mezi tématy uvnitř nápovědy uvádějte v relativních cestách ve vztahu k umístění cílových a zdrojových dokumentů.

[Dfiles.lst]: mdata/files.lst.md "files.lst"
[Dkeywords.lst]: mdata/keywords.lst.md "keywords.lst"
[Dtree.lst]: mdata/tree.lst.md "tree.lst"
[Dfts-keywords.lst]: fulltextIndex.md "fts-keywords.lst"
[configDesc]: helpCfg.md ""
[Dkeywords-files.lst]: mdata/keywords-files.lst.md "keywords-files.lst"
[newLang]: newLang.md ""
[build]: publish.md ""
