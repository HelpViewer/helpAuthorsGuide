# 🔗 Odkazy v textech

- Dvojí podtržítko (**__**) zastupuje vybraný jazyk, který si systém automaticky doplní ze stavu uživatelského nastavení.
- Odkazy na dokumenty uvádějte v relativních cestách (s použitím ..). 
- Lomítka v cestách používejte **dopředná - /**.
- V případě složitějších odkazů (přechod do jiné nápovědy) používejte **?** a zadejte pouze parametry, aby byl přenos systému do budoucna jednodušší

Níže naleznete obvyklé způsoby definice odkazu.

## Uvnitř nápovědy

### Jiné téma/stránka
```
Spusťte prohlížeč bez [CORS omezení][bypassCORS] nebo budete vidět pouze prázdnou stránku.
// ... na konci souboru:
[bypassCORS]: corsPolicy.md "Prohlížeč může blokovat přístup k místním souborům (file://) kvůli CORS politikám"
```
Spusťte prohlížeč bez [CORS omezení][bypassCORS] nebo budete vidět pouze prázdnou stránku.

### Jiné téma a jeho podkapitola
```
Kapitola [Jak aplikace pracuje][working] pojednává o základech práce s aplikací.
// ... na konci souboru:
[working]: README.md#how-it-works "Jak aplikace pracuje"
```
*Zde se s jazykovým překladem kapitol bude automaticky měnit také vytvořený odkaz.*

Kapitola [Jak aplikace pracuje][working] pojednává o základech práce s aplikací.

## Mimo nápovědu - URI cesta
```
Toto řešení používá také [JSZip knihovnu][JSZIP].
// ... na konci souboru:
[JSZIP]: http://jszip.org/ "JSZip - práce se ZIP soubory"
```
Toto řešení používá také [JSZip knihovnu][JSZIP].

## Jiný soubor nápovědy

### Výchozí stránka
```
Uvidíte [uživatelskou dokumentaci][userdoc] přímo v HelpViewer, podobně jako teď vidíte tento web.
// ... na konci souboru:
[userdoc]: ?d=hlp-user/Help-__.zip "Rychlá příručka pro uživatele"
```

Uvidíte [uživatelskou dokumentaci][userdoc] přímo v HelpViewer, podobně jako teď vidíte tento web.

### Konkrétní téma
```
Pokud potíže přetrvávají, přejděte k [příručce pro řešení problémů][trouble].
// ... na konci souboru:
[trouble]: ?d=hlp/Help-__.zip&p=trouble.md "Příručka pro řešemí problémů"
```

Pokud potíže přetrvávají, přejděte k [příručce pro řešení problémů][trouble].

### URI ze sítě
```
Uvidíte [uživatelskou dokumentaci][userdoc2] přímo v HelpViewer, podobně jako teď vidíte tento web.
// ... na konci souboru:
[userdoc2]: ?d=https://github.com/HelpViewer/helpUser/releases/download/20250615/Help-__.zip "Rychlá příručka pro uživatele"
```

Uvidíte [uživatelskou dokumentaci][userdoc2] přímo v HelpViewer, podobně jako teď vidíte tento web.

[bypassCORS]: corsPolicy.md "Prohlížeč může blokovat přístup k místním souborům (file://) kvůli CORS politikám"
[working]: README.md#how-it-works "Jak aplikace pracuje"
[JSZIP]: http://jszip.org/ "JSZip - práce se ZIP soubory"
[userdoc]: ?d=hlp-user/Help-__.zip "Rychlá příručka pro uživatele"
[trouble]: ?d=hlp/Help-__.zip&p=trouble.md "Příručka pro řešemí problémů"
[userdoc2]: ?d=https://github.com/HelpViewer/helpUser/releases/download/20250615/Help-__.zip "Rychlá příručka pro uživatele"
