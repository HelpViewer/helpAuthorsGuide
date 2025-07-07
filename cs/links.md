# 🔗 Odkazy v textech

- Dvojí podtržítko (**__**) zastupuje vybraný jazyk, který si systém automaticky doplní ze stavu uživatelského nastavení.
- Odkazy na dokumenty uvádějte v relativních cestách (s použitím ..). 
- Lomítka v cestách používejte **dopředná - /**.
- V případě složitějších odkazů (přechod do jiné nápovědy) používejte **?** a zadejte pouze parametry, aby byl přenos systému do budoucna jednodušší

Níže naleznete obvyklé způsoby definice odkazu.

## Uvnitř nápovědy

### Jiné téma/stránka
```markdown
Soubor definuje propojení [klíčových slov][Dkeywords.lst] a [seznamu souborů][Dfiles.lst]
// ... na konci souboru:
[Dfiles.lst]: mdata/files.lst.md "files.lst"
[Dkeywords.lst]: mdata/keywords.lst.md "keywords.lst"
```
Soubor definuje propojení [klíčových slov][Dkeywords.lst] a [seznamu souborů][Dfiles.lst]

### Jiné téma a jeho podkapitola
```markdown
Kapitola [Jak aplikace pracuje][working] pojednává o základech práce s aplikací.
// ... na konci souboru:
[working]: README.md#how-it-works "Jak aplikace pracuje"
```
*Zde se s jazykovým překladem kapitol bude automaticky měnit také vytvořený odkaz.*

Kapitola [Jak aplikace pracuje][working] pojednává o základech práce s aplikací.

## Mimo nápovědu - URI cesta
```markdown
Toto řešení používá také [JSZip knihovnu][JSZIP].
// ... na konci souboru:
[JSZIP]: http://jszip.org/ "JSZip - práce se ZIP soubory"
```
Toto řešení používá také [JSZip knihovnu][JSZIP].

## Jiný soubor nápovědy

### Výchozí stránka
```markdown
Uvidíte [uživatelskou dokumentaci][userdoc] přímo v HelpViewer, podobně jako teď vidíte tento web.
// ... na konci souboru:
[userdoc]: ?d=hlp-user/Help-__.zip "Rychlá příručka pro uživatele"
```

Uvidíte [uživatelskou dokumentaci][userdoc] přímo v HelpViewer, podobně jako teď vidíte tento web.

### Konkrétní téma
```markdown
Pokud potíže přetrvávají, přejděte k [příručce pro řešení problémů][trouble].
// ... na konci souboru:
[trouble]: ?d=hlp/Help-__.zip&p=trouble.md "Příručka pro řešemí problémů"
```

Pokud potíže přetrvávají, přejděte k [příručce pro řešení problémů][trouble].

### URI ze sítě
```markdown
Uvidíte [uživatelskou dokumentaci][userdoc2] přímo v HelpViewer, podobně jako teď vidíte tento web.
// ... na konci souboru:
[userdoc2]: ?d=https://github.com/HelpViewer/helpUser/releases/download/20250615/Help-__.zip "Rychlá příručka pro uživatele"
```

Uvidíte [uživatelskou dokumentaci][userdoc2] přímo v HelpViewer, podobně jako teď vidíte tento web.

[Dfiles.lst]: mdata/files.lst.md "files.lst"
[Dkeywords.lst]: mdata/keywords.lst.md "keywords.lst"
[working]: README.md#how-it-works "Jak aplikace pracuje"
[JSZIP]: http://jszip.org/ "JSZip - práce se ZIP soubory"
[userdoc]: ?d=hlp-user/Help-__.zip "Rychlá příručka pro uživatele"
[trouble]: ?d=hlp/Help-__.zip&p=trouble.md "Příručka pro řešemí problémů"
[userdoc2]: ?d=https://github.com/HelpViewer/helpUser/releases/download/20250615/Help-__.zip "Rychlá příručka pro uživatele"
