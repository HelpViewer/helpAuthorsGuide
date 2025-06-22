# 🔑 Token

Ke správné funkci vydání je potřeba založit uživatelský GitHub token.

Pokud token nebude s repozitářem propojen a nebo vyprší, sestavovací skript bude selhávat při pokusu o nahrání vygenerované nápovědy do příloh vydání.

## Založení PAT tokenu

1. Otevřete: 
```
https://github.com/settings/personal-access-tokens
```

2. Fine-grained personal access tokens
3. Generate new token
4. Jméno zvolte podle sebe
5. Resource owner bude Vaše organizace nebo Vy jako uživatel
6. Expiration nastavte hodnotu co nejvyšší
7. Repository access: Only select repositories (dále vyberte konkrétní repozitář s Vaší nápovědou)
8. Nastavte v tokenu následující oblasti a úroveň oprávnění:

| Oblast | Úroveň |
|---|---|
| Actions | Read and write |
| Commit statuses | Read and write |
| Contents | Read and write |
| Deployments | Read and write |
| Environments | Read and write |
| Merge queues | Read and write |
| Metadata | Read-only |
| Pull requests | Read and write |
| Webhooks | Read and write |
| Workflows | Read and write |

9. Generate token
10. V zeleném rámečku uvidíte kód tokenu, který si uložte. Nereloadujte, kód byste už znovu nezískali. (Pokud nešťastně reloadnete, klikněte na název tokenu. Otevře se detail a zde klikněte na **Regenerate token**, potvrďte Expiration a uvidíte nový kód tentokrát v modrém poli.)

## Propojení tokenu s repozitářem nápovědy

Je potřeba provést tyto kroky:

1. Otevřete: 
```
https://github.com/(organizace)/(repozitář)/settings/secrets/actions
```
(
- Na kartě repozitáře nahoře:
- napravo Settings
- Nalevo dole: Secrets and variables
- Actions

)
 
2. Napravo: Repository secrets
3. New repository secret
4. Name: **_TOKEN** (jméno nelze změnit)
5. Vložte kód který jste si uschovali z předešlého kroku
6. Add secret

Nyní by měl proces sestavení nápověd fungovat správně.
