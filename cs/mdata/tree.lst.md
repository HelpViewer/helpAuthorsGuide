# 📖Strom témat (tree.lst)

- > [!WARNING] Tento formát je velmi přísný, prosím, dodržujte pravidla přesně.
- Soubor definuje hierarchickou strukturu kapitol nápovědy
- Není povinné, aby všechny soubory byly jeho součástí
- Jeden řádek = jedna položka stromu
- Zalomení řádku uprostřed definice není povoleno

## Struktura souboru

```
[1]|[2]|[3]|[4]|[5]
```

## Popis pozic

| Pozice | Popis |
|---|---|
| [1] | Jedna mezera = jedna podúroveň (zanoření). Bez mezer = hlavní úroveň |
| [2] | Titulek položky ve stromě |
| [3] | Text bublinové nápovědy při najetí myši nad položku |
| [4] | Prázdné nebo platná relativní cesta k obrázku, který má být na levou stranu položky připojen |
| [5] | Relativní cesta cílového souboru s obsahem kapitoly nebo speciání názvy níže |

### Pozice [5]: speciální názvy

| Hodnota | Popis |
|---|---|
| =latestApp | Vyhledá URI pro poslední verzi HelpViewer |
| =latestHelp | Vyhledá URI pro poslední verzi souboru nápovědy (pokud je repozitář hostován na GitHub jako veřejný) |
| :(...) | Relativní cestu systém vezme z dat aplikace, nikoli nápovědy. V této chvíli je **viewRepo.htm** jedinou vhodnou hodnotou. |
| ~~ | Pokud se v cestě někde objeví tyto znaky, pak budou nahrazeny verzí otevřeného balíku nápovědy. |
