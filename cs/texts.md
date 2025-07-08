# 📝 Texty kapitol

HelpViewer předpokládá, že text bude ve znakové sadě **UTF-8 no BOM (65001)**.

V rámci textu kapitol můžete použít veškerou standardní syntaxi **[md][MDSyntax]** dokumentu jako například **#** značku s nadpisy až do úrovně 6 (tedy například **###### Nadpis**). Tyto nadpisy pak **HelpViewer** použije, aby automaticky sestavil seznam částí (🔖) a nabídl jej uživateli k procházení. Pokud kromě **h1** nebude v kapitole žádný další nadpis, seznam se uživateli nenabídne.

Také můžete md kód v případě potřeby prokládat s html nebo javascript kódem.

V dalších podkapitolách této sekce jsou uvedeny další informace, které byste měli znát a také funkce HelpViewer, které můžete použít.

## Ikonky

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