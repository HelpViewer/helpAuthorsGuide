# 📝 Texty kapitol

HelpViewer předpokládá, že text bude ve znakové sadě **UTF-8 no BOM (65001)**.

V rámci textu kapitol můžete použít veškerou standardní syntaxi **[md][MDSyntax]** dokumentu jako například **#** značku s nadpisy až do úrovně 6 (tedy například **###### Nadpis**). Tyto nadpisy pak **HelpViewer** použije, aby automaticky sestavil [seznam částí][SecList] (🔖).

Také můžete md kód v případě potřeby prokládat s html nebo javascript kódem.

V dalších podkapitolách této sekce jsou uvedeny další informace, které byste měli znát a také funkce HelpViewer, které můžete použít.

## 🖼️ Ikonky

V rámci textu můžete vkládat také unicode znaky. Některé z nich představují ikonky, které je možno použít bez nutnosti další externí knihovny.

Vložení do textu kapitoly provedete buďto přímou kopií znaku, nebo vložením dalších dvou jiných tvarů (HTML znakové entity):
```markdown
💡
&amp;#128161;
&amp;#x1F4A1;
```

Pro konkrétní kódy a situace doporučuji použití Copilot/ChatGPT, které Vám pomohou rychle najít vhodné příklady.

💡 Tisk ikon je ve výchozím stavu vypnutý. Více v [tisk ikonek][IconPrint].

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
[SecList]: sectionList.md "Seznam částí"
[IconPrint]: print.md#h-2-0 "Tisk ikonek"
