# 🔑 Token

For the release to work properly, you need to create a PAT GitHub user token.

If the token is not linked to the repository or expires, the build script will fail when trying to upload the generated help to the release attachments.

## Creating a PAT token

1. Open: 
```
https://github.com/settings/personal-access-tokens
```

2. Fine-grained personal access tokens
3. Generate new token
4. Choose a name according to yourself
5. Resource owner will your organisation or you as a user
6. Expiration set the value as high as possible
7. Repository access: Only select repositories (then select the specific repository with your help)
8. Set the following areas and permission levels in the token:

| Area | Level |
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
10. In the green box you will see the token code to save. Do not reload, you would not get the code again. (If you accidentally reload, click on the token name. This will bring up the detail, and here click on **Regenerate token**, confirm Expiration and you will see the new code this time in the blue box.)

## Linking the token to the help repository

The following steps need to be taken:

1. Open: 
```
https://github.com/(organizace)/(repozitář)/settings/secrets/actions
```
(
- On the repository tab at the top:
- On right: Settings
- On left down: Secrets and variables
- Actions

)
 
2. On right: Repository secrets
3. New repository secret
4. Name: **_TOKEN** (name cannot be changed)
5. Enter the code you saved from the previous step
6. Add secret

The hint build process should now work correctly.
