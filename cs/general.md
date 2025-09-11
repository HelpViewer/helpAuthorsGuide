# 💡 Obecná doporučení a zdroje informací

V organizaci **[HelpViewer][HV]** naleznete repozitáře začínající na **help\***. Kromě **helpTemplate** a **HelpViewer** jsou všechny ukázkami souborů nápovědy. Můžete si vzít kterýkoli z nich jako příklad, stáhnout si z kteréhokoli **Release** jeho přílohy **Help-*.zip**. Archivy jsou nezaheslované, jejich obsah je přístupný k procházení.

Během přípravy Vaší nápovědy ji můžete offline procházet i přesto, že nebyla ještě vydána a ověřit si tak výsledky. Provedete to následujícím způsobem - spustíte **HelpViewer** v prohlížeči s procházením místního souboru a předáte mu relativní cestu ke své vznikající nápovědě:
```
file://.../HelpViewer/?d=../VaseNapoveda/__/
```

- __ zastupuje zkratku uživatelem zvoleného jazyka
- Pokud by cesta nefungovala, lomítka **/** v d nahraďte za **%2F**
- Fulltextové vyhledávání bude po dobu těchto testů nefunkční (index je sestaven automaticky až při vydávání)

Fráze **[pub]** v textové zprávě komitu spouští přípravu Release. V rámci tohoto komitu mějte připraven popis na začátku CHANGELOG.md souboru. Tento popis se použije do textu Release.

[HV]: https://github.com/orgs/HelpViewer/repositories "Repozitáře"
