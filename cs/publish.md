# 📦Vydání verze nápovědy

💡 Doporučení:
- Pokud neznáte **Git**, projděte si jeho [dokumentaci][GitRef].

✅ Vstupní podmínky:
- Ujistěte se, že máte s repozitářem nápovědy správně propojený [🔑 PAT Token][PATToken], který nevypršel. Pokud nebude token platný, vydávací skript selže.

Zjednodušený postup pro vydání nápovědy lze shrnout takto:

1. Otevřete terminál/příkazovou řádku
2. Přejděte ke svému repozitáři
3. Přidejte veškeré své nesloučené změny:
```
git add .
```
4. Slučte změny do repozitáře:
```
git commit -m "Úpravy nápovědy"
```
"Úpravy nápovědy" - zde může být jakákoli Vaše popisná zpráva

5. Připravte změnu v souboru **CHANGELOG.md** na kořeni repozitáře tak, aby začátek souboru vypadal:
```
# Changelog

## rokměsícden
- Moje změny
```

kde:

| Pozice | Popis |
|---|---|
| rokměsícden | bude datum ve formátu 202050622 (rok, měsíc a den bez oddělovačů) |
| Moje změny | Zápis vašich popisů změn |

6. Slučte změny do repozitáře:
```
git commit -m "Úpravy nápovědy [pub]"
```
- "Úpravy nápovědy" - zde může být jakákoli Vaše popisná zpráva
- **[pub]** v textu zprávy je nutný, aby byl spuštěn vydávací skript

7. Slučte svou verzi do GitHub serveru:
```
git push
```

Pak dojde ke spuštění vydávacího skriptu. 

Výsledkem bude vydání s přílohami:
- Help-(zkratka jazyka).zip (pro každý jednotlivý jazyk)
- Help-.zip (pro [Vlastní UI prohlížeče][CustomUI])

[GitRef]: https://git-scm.com/docs "Git"
[PATToken]: token.md "GitHub PAT token"
[CustomUI]: customUI.md "Vlastní UI prohlížeče"
