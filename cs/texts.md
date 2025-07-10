# 📝 Texty kapitol

HelpViewer předpokládá, že text bude ve znakové sadě **UTF-8 no BOM (65001)**.

V rámci textu kapitol můžete použít veškerou standardní syntaxi **[md][MDSyntax]** dokumentu jako například **#** značku s nadpisy až do úrovně 6 (tedy například **###### Nadpis**).

Také můžete md kód v případě potřeby prokládat s html nebo javascript kódem.

V dalších podkapitolách této sekce jsou uvedeny další informace, které byste měli znát a také funkce HelpViewer, které můžete použít.

## 🔖 Seznam částí

**HelpViewer** automaticky sestaví z nadpisů (h1-6, # ... ######), seznam částí (🔖) a nabídne jej uživateli k rychlému a pohodlnému procházení textem kapitoly. 

- Pokud dokument obsahuje pouze hlavní nadpis (h1 / #), žádný seznam se nezobrazí.
- Přehled je dostupný, pokud se v dokumentu nachází alespoň jeden další nadpis.

Záložky jsou automaticky pojmenovávány v tomto formátu: #h-(úroveň)-(pořadí).
  - úroveň je číslo od 1 do 6 podle úrovně nadpisu (h1 = 1, ..., h6 = 6)
  - pořadí je index od 0, který určuje pořadí výskytu nadpisů dané úrovně v rámci celé kapitoly

Určování pořadí:
- Počítadlo je oddělené pro každou úroveň (h1 má svůj vlastní čítač, h2 jiný atd.)
- Pořadí se přiděluje při načítání dokumentu zleva doprava, shora dolů.
- ⚠ Pokud do dokumentu vložíte nový nadpis (např. mezi dvě stávající), automaticky převezme index nadpisu, který byl na jeho místě. Nadpisy následující za ním se o jedno pořadí posunou.

Tímto je zajištěno, že záložky zůstanou konzistentní a předvídatelné, i když se struktura dokumentu v budoucnu změní.

## 🖼️ Ikonky

V rámci textu můžete vkládat také unicode znaky. Některé z nich představují ikonky, které je možno použít bez nutnosti další externí knihovny.

Vložení do textu kapitoly provedete buďto přímou kopií znaku, nebo vložením dalších dvou jiných tvarů (HTML znakové entity):
```markdown
💡
&amp;#128161;
&amp;#x1F4A1;
```

Pro konkrétní kódy a situace doporučuji použití Copilot/ChatGPT, které Vám pomohou rychle najít vhodné příklady.

### Ikonky a tisk

Před přípravou tisku jsou ikonky automaticky odebírány z textu. Pokud Vám toto chování nevyhovuje, můžete jej upravit buď na úrovni konfigurace celé nápovědy, nebo pomocí direktivy v konkrétním tématu.

Chcete-li ikonky zachovat v konkrétním tématu, vložte tuto direktivu po prvním nadpisu kapitoly (nesmí být před nadpisem) nebo později v textu tématu:

```markdown
# &#128214;Help Viewer přehled

<!-- @print-keep-icons -->
Aplikace je rozdělena na dvě hlavní oblasti:
```

⚠️ Upozornění: Direktivu napište s přesnou mezerou, jak je ukázáno, a nekombinujte ji s jinými komentáři nebo bloky. Díky tomu bude zpracování správné a bez problémů.

Chcete-li ikonky zachovat ve všech tématech, nastavte konfigurační volbu nápovědy **OverridePrintKeepIcons** na 1.

Podrobnější popis chování:

| OverridePrintKeepIcons | print-keep-icons | Výsledek |
|---|---|---|
| 0 / není | není | ikonky odebrány |
| 1 | není | ikonky zachovány |
| 0 | je | ikonky zachovány |
| 1 | je | ikonky odebrány |

## Seznamy

Odrážkové seznamy nezbytně musí mít mezeru za označením (číslo u číslovaného, - u nečíslovaného seznamu):

```markdown
- Odrážka2
1. Odrážka2
```

Ukázky (dvojice - chybně a správně):

A)

-Odrážka1
- Odrážka2

B)

1.Odrážka1
1. Odrážka2

## Odstavce

U **md** je odstavce v textu nutno vytvářet pomocí volného řádku mezi nimi:
```markdown
První odstavec

Druhý odstavec
```

Ukázka:

První odstavec

Druhý odstavec

## Dvojmezera na konci řádku

Pokud použijete v textu na konci řádku dvakrát mezeru a napíšete další řádek, zajistíte tím odsazení nového řádku na úroveň předešlého:

```
  - ☰ Zobrazit levý panel__
    *(pokud je skrytý)*
```
Ve výpisu mezery zastupují _ (jsou dvě), aby byly viditelné.

Ukázka:

  - ☰ Zobrazit levý panel  
    *(pokud je skrytý)*

## Uzavíratelná sekce

Prostým html kódem vytvoříte uzavíratelnou sekci. Zobrazovací logika ji správně převede do výstupu pro uživatele. 

```html
<details>
<summary>Zde je hlavní nadpis. Kliknutím na něj se rozbalí další informace</summary>
Zde je zobrazen další popis dané problematiky.
</details>
```

Ukázka:
<details>
<summary>Zde je hlavní nadpis. Kliknutím na něj se rozbalí další informace</summary>
Zde je zobrazen další popis dané problematiky.
</details>

[MDSyntax]: https://www.markdownguide.org/basic-syntax/ "MD syntaxe"