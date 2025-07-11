# 🔖 Seznam částí

**HelpViewer** automaticky sestaví z nadpisů (h1-6, # ... ######), seznam částí (🔖) a nabídne jej uživateli k rychlému a pohodlnému procházení textem kapitoly. 

## Viditelnost
- Pokud dokument obsahuje pouze hlavní nadpis (h1 / #), žádný seznam se nezobrazí.
- Přehled je dostupný, pokud se v dokumentu nachází alespoň jeden další nadpis.

## Formát jmen záložek

Záložky jsou automaticky pojmenovávány v tomto formátu: #h-(úroveň)-(pořadí).
  - úroveň je číslo od 1 do 6 podle úrovně nadpisu (h1 = 1, ..., h6 = 6)
  - pořadí je index od 0, který určuje pořadí výskytu nadpisů dané úrovně v rámci celé kapitoly

## Určení pořadí záložek

- Počítadlo je oddělené pro každou úroveň (h1 má svůj vlastní čítač, h2 jiný atd.)
- Pořadí se přiděluje při načítání dokumentu zleva doprava, shora dolů.

## Změny v nadpisech dokumentů

⚠️ Pokud do dokumentu vložíte nový nadpis (např. mezi dvě stávající), automaticky převezme index nadpisu, který byl na jeho místě. Nadpisy následující za ním se o jedno pořadí posunou.

Tímto je zajištěno, že záložky zůstanou konzistentní a předvídatelné, i když se struktura dokumentu v budoucnu změní.
