# 📇 Seznam klíčových slov (keywords.lst)

- > [!WARNING] Tento formát je velmi přísný, prosím, dodržujte pravidla přesně.
- Soubor definuje seznam klíčových slov nápovědy
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
| [1] | Klíčové slovo |
| [2] | Nepovinné. Synonymum pro dané slovo. Pokud má být použito, vždy mu předchází středník (**;**) a může se libovolně krát opakovat. |

## Pravidla

- Mezera není oddělovačem slova
- Řádek nikdy nekončí středníkem
- Alespoň pozice [1] musí být definována
- Synonyma jsou rozložena na jednotlivá slova a uživateli je pro všechna tato slova nabízen stejný seznam témat (**keywords-files.lst**)
- V případě, že se synonyma budou překrývat napříč řádky (vyskytne se jedno synonymum na více řádcích), HelpViewer sestaví sloučený seznam témat ve kterém bude každé téma jen jednou (rozhodne se zde podle files.lst)
