# az login


# create user
az ad sp create-for-rbac \
  --name "GitHub-Actions-SP" \
  --role contributor \
  --scopes /subscriptions/<sub_id> \
  --sdk-auth