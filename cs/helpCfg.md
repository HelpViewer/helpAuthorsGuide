# 🛠️ Konfigurace nápovědy

Konfiguraci nápovědy změníte v souboru **_config.txt**. Soubor se nachází v podsložce jazykové verze nápovědy. Každý jazyk má svoji vlastní verzi.

Jeho základní stuktura je tato:

```
klíč|hodnota
klíč|hodnota
```

## Pravidla

- 1 řádek = jedna hodnota
- Pokud se klíč bude později opakovat, je použita vždy poslední z přečtených hodnot

## Konfigurační klíče

### Ikony stromu témat

| Jméno klíče | Popis a význam |
|---|---|
| OverrideBookIcon-opened | Znak pro otevřenou knihu |
| OverrideBookIcon-closed | Znak pro zavřenou knihu |

### Přepsání uživatelských nastavení UI

| Jméno klíče | Popis a význam |
|---|---|
| OverrideColorTheme | Přepíše uživatelské schéma barev na konkrétní jiné a uloží hodnotu do konfigurace uživatele |
| OverrideSidebarVisible | Přepíše uživatelskou volbu, zda bude levý panel viditelný a uloží hodnotu do konfigurace uživatele |
| HOME | Nastaví relativní cestu první obrazovky nápovědy. Výchozí hodnota: README.md |

### Přepsání výchozího chování UI

| Jméno klíče | Popis a význam |
|---|---|
| OverridePrintKeepIcons | Přepíše výchozí chování odebírání HTML ikonek při tisku. Výchozí: 0. 1 = tisk textu včetně ikonek. Direktiva \<\!-- @print-keep-icons --\> v textu tématu logiku této konfigurace pro konkrétní téma obrací do opačného stavu. |

### Klíče, které řídí proces vydávání
| Jméno klíče | Popis a význam |
|---|---|
| _lang | Jazyk tohoto balíku nápovědy |
| _langs | Seznam všech jazyků nápovědy, které byly v daném procesu vydání zpracovány. Slouží jako jeden ze zdrojů seznamu 🌐. |
| _version | Verze vydání (převzata ze souboru CHANGELOG.md) |
| _prjname | (organizace)/(jméno repozitáře) ve kterém se nápověda v době sestavení nacházela. |
