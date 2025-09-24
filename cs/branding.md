# 🏷️ Vizuální identita

Pro úpravu výchozí identity aplikace na Vaši vlastní vizuální identitu poskytuje **HelpViewer** nástroje, které jsou popsané v následujících podkapitolách.

Pro některé nástroje stačí přidání souborů do Vaší nápovědy. Pro jiné je nutná změna konfigurace, případně znalost CSS nebo javascriptu.

Aby se změny projevily pro uživatele, je nutné nápovědu vždy znovu přeložit (vydat novou verzi). Jinak se nové soubory nebo úpravy CSS/JS neprojeví.

## Snadné úpravy

### 🌅 První obrazovka

- První obrazovku představuje **README.md** soubor umístěný v kořeni jazykové verze nápovědy.
- Tento soubor se otevírá jako první, když čtenář spustí nápovědu.

### 🌐 Vlastní ikona aplikace v záhlaví stránky (favicon)

- Do repozitáře nápovědy vložte soubor:
**helpProjekt/_base/favicon.png**

### 📖 Ikony stromu témat

- Možnost změn ikon ve stromu témat je popsána v kapitole [Ikony stromu témat][TocIcon].

## Konfigurační úpravy

### 🎨 Náhrada nebo rozšíření kaskádového stylu

- Jak postupovat při nahrazení nebo rozšíření kaskádových stylů je popsáno v kapitole 🛠️ [Vlastní UI prohlížeče][customUI].
- Pamatujte, že některé definice (např. názvy CSS tříd nebo hodnoty atributu id) lze měnit jen s určitými omezeními.
- V souboru hvdata/data.zip:**main.css** se na začátku nachází pseudotřída **:root**, která obsahuje konstanty barevné palety. Pro úvodní úpravy Vám může postačovat právě změna hodnot zde.
- V rámci pseudotřídy **:root**, kterou byste definovali v **plus.css** můžete dodatečně změnit písmo rozhraní celé aplikace.
- CSS3 dovoluje definovat [vizuální efekty a přechody][CSS3Effects]. Dalším zdrojem může být i článek [Web Visual Effects with CSS3][CSS3Effects2].

#### 🖌️ Změna barev a písma

Níže je ukázka, jak nastavit globální proměnné pro barvy a písmo. Tyto proměnné pak můžete použít kdekoli v CSS přes `var()`.

```css
:root {
  --color-bg: black;
  --color-fg: white;
  --font: "Segoe UI", Roboto, sans-serif; /* hlavní písmo */
}

body {
  font-family: var(--font);
  background: var(--color-bg); /* použití proměnné */
  color: var(--color-fg, silver); /* použití proměnné se záložní hodnotou, pokud chybí */
}
```

Pokud je to možné, používejte přednostně CSS proměnné. Usnadňuje to budoucí změny barev, písma nebo dalších parametrů.

#### 🖱️ Definice vlastního kurzoru

- Vlastní kurzor můžete definovat v **plus.css** například takto:

```css
:root {
  cursor: url('muj-kurzor.png'), auto;
}
```

Soubor **muj-kurzor.png** musí být v relativním umístění k **index.html** a nemůže být součástí nápověd nebo dat (nemůže být v ZIP archivu).

#### ✨ Úvodní obrazovka

- Obrazovka vyplní celou viditelnou plochu a slouží k rychlé prezentaci - typicky produktová ikona, název a krátký slogan.- Do repozitáře nápovědy vložte pro každý jazyk soubor:
**helpProjekt/(jazyk)/_splash.md** :

```markdown
# _![HelpViewer](media/HV.png)

# HelpViewer

## Vaše nápověda - Přehledně - Rychle - Bez kompilace
```

(podtržítko v prvním nadpisu znamená definici neodebírej pro plugin pTR1stHeadingToTopPanel)

- Pokud je v nasazeném balíčku aplikace zahrnut 🖥️ puiSplash (Úvodní obrazovka), při prvním otevření 🌅 první obrazovky se jako první informace uživateli zobrazí právě tato obrazovka.

- Pro úpravu jejího vzhledu je potřeba definovat **helpProjekt/_base/plus.css** a v něm například toto:

```css
.splash {
  gap: 3rem;
  font-size: calc(1em * 1.5);
  background: radial-gradient(circle, var(--c-contentPaneColor) 10%, var(--c-backgroundHead) 100%);
}

.splash h2 {
  text-align: center;
  word-wrap: break-word;
  overflow-wrap: break-word;
  hyphens: manual;
}
```

### 🧩 Pokročilé nástroje, programování

- Některé nástroje v dalších kapitolách mohou být omezené nebo nefunkční v závislosti na způsobu nasazení či konfiguraci ve vašem prostředí. Pro informace o stažení a instalaci balíčku se obraťte na svého systémového administrátora.
- Nástroje vyžadují minimálně konfiguraci. U některých je potřeba doprogramování zdrojóvého kódu při spouštění nápovědy (helpProjekt/_base/**plus.js**).
- Tyto pokročilé možnosti jak upravit identitu aplikace popisuje 🧩 [Dokumentace pro vývojáře][DGuide].
- K dispozici je také automatizovaně generovaná dokumentace běžící instance, která je přístupná přes plugin 🧩 [Prohlížeč objektů][oexplorer] v 🐞 ladícím režimu. Ladící režim není standardně povolen v produkčním prostředí.
- Aplikaci lze stáhnout jako:
  - 🚀 kompletní balíček (ZIP)
  - 📥 vlastní balíček (ZIP)
  - 🐳 [Docker/Podman kontejner][DCONT]

### 💧 Vodoznak

- Funkcionalitu zajišťuje plugin 🖥️ puiWatermark (Vodoznak na panelu s textem kapitoly), který je nutno doplnit konfigurací.

### 🖼️ Vlastní ikony pro tlačítka

- Ikony tlačítek lze měnit konfiguračně u pluginů odvozených z 🖥️ puiButton. Každý plugin má konfigurační volbu ⚙️ CAPTION s výchozí hodnotou.
- Pro změnu ikon bude možná potřeba v rámci souboru nápovědy šířit vlastní soubor písma (umístěte do adresáře **_base**).

### 💬 Texty a tooltipy

- Popisky a překlady aplikace jsou řízené lokalizací, která je součástí dat aplikace.
- Více informací najdete v kapitolách:
  - 🌐 [Nový jazyk prohlížeče][DGuideLangCentral] - hlavní lokalizační data
  - 🌐 [Lokalizace pluginů][DGuideLangPlug] - lokalizační data jednotlivých pluginů
- V rámci těchto změn stačí konfigurační úpravy. Zásah do kódu obvykle není potřeba.

#### © Copyright, ® registrováno a ™ ochranná známka

- Texty copyrightu, registrovaných vzorů, ochranných známek a výzvy je nutné do aplikace doplnit dle vlastních potřeb.
- Žádná zvláštní podpora na úrovni programu pro tuto oblast není nyní implementována.
- Zde je nutné programování a ruční změna nebo rozšíření balíčku aplikace.
- Aplikace je šířena pod otevřenou licencí [MIT][MIT]. Kód můžete měnit a šířit komerčně i nekomerčně, ale musíte zachovat licenci **HelpViewer** a původní copyright ve vlastních balíčcích.

[TocIcon]: tocIcon.md "Ikony stromu témat"
[customUI]: customUI.md "Vlastní UI prohlížeče"
[DGuide]: ?d=hlp-dguide/Help-__.zip "Dokumentace pro vývojáře"
[DGuideLangCentral]: ?d=hlp-dguide/Help-__.zip&p=newLangViewer.md "Nový jazyk prohlížeče"
[DGuideLangPlug]: ?d=hlp-dguide/Help-__.zip&p=plugLocStrings.md "Lokalizace pluginů"
[oexplorer]: ?d=hlp-dguide/Help-__.zip&p=oexplorer.md "Prohlížeč objektů"
[DCONT]: https://github.com/HelpViewer/HelpViewer/pkgs/container/helpviewer "Kontejner"
[CSS3Effects]: https://prismic.io/blog/css-image-effects "50 Creative CSS Image Effects for Engaging Websites"
[CSS3Effects2]: https://leanpub.com/web-visual-effects-with-css3/read "Web Visual Effects with CSS3"
[MIT]: https://github.com/HelpViewer/HelpViewer/blob/master/LICENSE "MIT licence"
