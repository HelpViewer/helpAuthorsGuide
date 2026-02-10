# 🖨️ Tisk

## 🖼️ Ikonky

Před přípravou tisku jsou ikonky automaticky odebírány z textu. Pokud Vám toto chování nevyhovuje, můžete jej upravit buď na úrovni konfigurace celé nápovědy, nebo pomocí direktivy v konkrétním tématu.

Chcete-li ikonky zachovat v konkrétním tématu, vložte tuto direktivu po prvním nadpisu kapitoly (nesmí být před nadpisem) nebo později v textu tématu:

```markdown
# &#128214;Help Viewer přehled

<!-- @print-keep-icons -->
Aplikace je rozdělena na dvě hlavní oblasti:
```

> [!WARNING]
> Direktivu napište s přesnou mezerou, jak je ukázáno, a nekombinujte ji s jinými komentáři nebo bloky. Díky tomu bude zpracování správné a bez problémů.

Chcete-li ikonky zachovat ve všech tématech, nastavte konfigurační volbu nápovědy **OverridePrintKeepIcons** na 1. Podrobnější popis chování:

| Override Print Keep Icons | print-keep-icons | Výsledek |
|---|---|---|
| 0 / není | není | ikonky odebrány |
| 1 | není | ikonky zachovány |
| 0 | je | ikonky zachovány |
| 1 | je | ikonky odebrány |

## Uzavíratelná sekce

Uzavíratelné sekce jsou před tiskem automaticky rozbaleny, aby se zajistil tisk veškerého textu.

## 📄 Zalomení stránky při tisku

V místě, kde potřebujete ručně zalomit stránku, vložte následující text do svého .md nebo .html souboru:

```markdown
<!-- @print-break -->
```

> [!WARNING]
> Text napište s přesnou mezerou, jak je zde ukázáno.

Při přípravě tiskové verze bude dokument na tomto místě automaticky rozdělen a následující obsah se vytiskne na nové stránce.
