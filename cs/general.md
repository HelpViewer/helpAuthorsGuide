# 💡Obecná doporučení a zdroje informací

V organizaci **[HelpVewer][HV]** naleznete repozitáře začínající na **help\***. Kromě **helpTemplate** a **HelpViewer** jsou všechny ukázkami souborů nápovědy. Můžete si vzít kterýkoli z nich jako příklad, stáhnout si z kteréhokoli **Release** jeho přílohy **Help-*.zip**. Archivy jsou nezaheslované, jejich obsah je přístupný k procházení.

Během přípravy Vaší nápovědy ji můžete offline procházet i přesto, že nebyla ještě vydána a ověřit si tak výsledky. Provedete to následujícím způsobem - spustíte **HelpViewer** v prohlížeči s procházením místního souboru a předáte mu relativní cestu ke své vznikající nápovědě:
```
file://.../HelpViewer/?d=../VaseNapoveda/__/
```

- Pokud by cesta nefungovala, lomítka **/** v d nahraďte za **%2F**
- Fulltextový bude po dobu těchto testů nefunkční (je sestaven automaticky až při vydávání)

[HV]: https://github.com/orgs/HelpViewer/repositories "Repozitáře"
