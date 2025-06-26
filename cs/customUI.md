# 🛠️ Vlastní UI prohlížeče

## Plné přepsání

1. V adresáři **HelpViewer** v **hvdata/data.zip** naleznete tyto soubory:
| Soubor | Popis |
|---|---|
| layout.htm | HTML kód rozhraní |
| appmainNext.js | Programová logika |
| main.css | CSS styl pro formátování vzhledu |

2. Extrahujte je
3. Založte složku **_base** v hlavním adresáři repozitáře nápovědy (na stejné úrovni jako adresáře s jazykovými verzemi)
4. Soubory zkopírujte do složky **_base**
5. Proveďte potřebné úpravy v těchto souborech

## Čisté rozšíření

Pokud chcete provést pouhé přidání funkcionality, pak přidejte do složky **_base** tyto soubory:

| Soubor | Popis |
|---|---|
| plus.css | CSS styl, který rozšíří nebo přepíše základní definice |
| plus.js | Rozšiřující programová logika pro stávající logiku prohlížeče |

## Výsledek

1. Při vydání nápovědy se začne nově vydávat další zip archiv **Help-.zip**
2. Tento soubor je nutné zahrnout do Vaší distribuce nápovědy, jinak se změny neprojeví
3. Vaše úpravy neovlivní HelpViewer u uživatelů. Ovlivní pouze způsob práce s konkrétní nápovědou ke které tyto úpravy připojíte

## Práce s nápovědou

- Při procházení nápověd je potřeba, aby uživatelé používali přístup k nápovědě ve formátu: **Help-__.zip**, aby HelpViewer zkoušel hledat tento základní soubor s úpravami
- Pokud by byl napřímo použit konkrétní jazyk, HelpViewer bude hledat uvnitř archivu nápovědy pro konkrétní jazyk (a soubory s ohledem na způsob distribuce nenajde)
- Pokud budou uživatele Vaše úpravy omezovat nebo budou nefunkční, bude jim plně postačovat smazat soubor **Help-__.zip** a obnoví tím původní funkčnost HelpViewer

## 💡 Doporučení
- Zdrojovým kódem rozhraní (rozzipovaných souborů) se inspirujte v implementaci vlastních úprav
- Zkontrolujte zda implementujete obvyklé funkcionality, které se chovají obvyklým způsobem
- Je žádoucí, aby se id názvy prvků neměnily (ideálně také v kódu nechyběly), neboť s nimi počítá i další logika aplikace, kterou touto implementací neměníte, pouze ji provoláváte v jiných scénářích
- Další logiku HelpViewer mimo tyto vyjmenované sobory nelze měnit souborem nápovědy. Jedinou možností změny je pak zásah do zdrojového kódu.
