# 📢 Vyznačené informační bloky (admonitions)

Implementace vyznačených informačních bloků vychází ze stylu admonitions běžně používaného v dokumentaci (např. GitHub Docs) a je navržena tak, aby byla s tímto stylem kompatibilní. Tuto součást aplikace může administrátor při instalaci odebrat - v takovém případě bude syntaxe stále platná, ale bloky se zobrazí jen jako běžný, zleva odsazený odstavec (blockquote).

- Notace psaní je **> [!TYP]Text informace.**
- Definovány jsou typy: NOTE, TIP, IMPORTANT, WARNING, CAUTION. Jakýkoli jiný typ se označí pouze stříbrnou čarou
- Odkazy uvnitř textu informace musí být uvedeny včetně cílové cesty uvnitř tohoto bloku (odkaz do zápatí stránky není dovolen - viz ukázka níže)

```markdown
> [!NOTE]**Poznámka**
Popis na dalším řádku.  
Popis na třetím řádku.

> [!TIP]Tip pro čtenáře
> [!IMPORTANT]Tento bod je významný.
Důležité upozornění pro bloky ```<script>``` si můžete přečíst na stránce s [ukázkou](innerJS.md "Ukázka") 

> [!WARNING]Pozor: žlutý vykřičník!

> [!CAUTION]Pozor: červený vykřičník!

> [!MYTEST]Blok neznámého typu
```

Ukázka:

> [!NOTE]**Poznámka**
Popis na dalším řádku.  
Popis na třetím řádku.

> [!TIP]Tip pro čtenáře
> [!IMPORTANT]Tento bod je významný.
Důležité upozornění pro bloky ```<script>``` si můžete přečíst na stránce s [ukázkou](innerJS.md "Ukázka") 

> [!WARNING]Pozor: žlutý vykřičník!

> [!CAUTION]Pozor: červený vykřičník!

> [!MYTEST]Blok neznámého typu

Kapitola 🏷️ [Vizuální identita][Branding] popisuje možnosti úpravy vzhledu těchto bloků, včetně definice vlastního typu bloku.

[Branding]: branding.md#h-3-8 "🏷️ Vizuální identita"
