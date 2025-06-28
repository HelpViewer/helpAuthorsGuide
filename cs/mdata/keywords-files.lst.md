# 📇Vazba klíčové slovo - soubor (keywords-files.lst)

- ⚠️ Tento formát je velmi přísný, prosím, dodržujte pravidla přesně.
- Soubor definuje propojení klíčových slov ([keywords.lst][Dkeywords.lst]) a seznamu souborů ([files.lst][Dfiles.lst])
- Jeden řádek = jedna položka
- Zalomení řádku uprostřed definice není povoleno
- Soubor je využíván v případě slovníků klíčových slov (📇)

## Struktura souboru

```
[1]
[1];[2]
```

## Popis pozic

| Pozice | Popis |
|---|---|
| [1] | Index propojeného souboru (počítáno od nuly) |
| [2] | Index propojeného souboru (počítáno od nuly). Opakování je přípustné, vždy je však před informací středník (**;**) |

## Pravidla
- Řádek nikdy nekončí středníkem
- Středník je oddělovačem propojení
- Každý řádek v tomto souboru odpovídá stejnému řádku v souboru s klíčovými slovy. Pokud si otevřete oba soubory vedle sebe, můžete je vnímat jako dva sloupce tabulky – odpovídající informace se nacházejí na stejných řádcích.

[Dfiles.lst]: mdata/files.lst.md "files.lst"
[Dkeywords.lst]: mdata/keywords.lst.md "keywords.lst"
