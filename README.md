# az login


# create user
az ad sp create-for-rbac \
  --name "GitHub-Actions-SP" \
  --role contributor \
  --scopes /subscriptions/<sub_id> \
  --sdk-auth

# Apply to Custom  Contributor Role

```bash
az ad sp create-for-rbac --name "GitHub-Actions-SP" --role 'infra_deploy' --scopes /subscriptions/
<sub id> --sdk-auth
```


# deploy changes
use to check the plans
az deployment group what-if --resource-group urlshortener-dev --template-file main.bicep 

to deploy
az deployment group  --resource-group urlshortener-dev --template-file main.bicep 