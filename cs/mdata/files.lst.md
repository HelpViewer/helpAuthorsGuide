# 📑Seznam souborů (files.lst)

- Soubor definuje seznam platných kapitol nápovědy
- Je doporučené, aby všechny soubory byly jeho součástí.
- Jeden řádek = jedna položka
- Zalomení řádku uprostřed definice není povoleno
- Soubor je využíván v případě slovníků klíčových slov (📇) a fulltext vyhledávání (🔎). V obou indexech nabízí popisné jméno souboru. V případě, že se soubor v seznamu neobjeví, zobrazí se jeho relativní cesta a název

## Struktura souboru

```
[1]|[2]
```

## Popis pozic

| Pozice | Popis |
|---|---|
| [1] | Relativní cesta k souboru |
| [2] | Titulek do slovníků. Je také záložním titulkem v případě přenačtení stránky bez kliknutí na seznamy v levém panelu |
