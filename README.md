### template-go-react [![Build Status](https://github.com/better-than-yours/template-go-react/workflows/frontend/badge.svg)](https://github.com/better-than-yours/template-go-react/frontend) [![Build Status](https://github.com/better-than-yours/template-go-react/workflows/backend/badge.svg)](https://github.com/better-than-yours/template-go-react/backend) [![Go Report Card](https://goreportcard.com/badge/github.com/better-than-yours/template-go-react)](https://goreportcard.com/report/github.com/better-than-yours/template-go-react)

### go deps

```sh
$ go mod tidy && go get -u
$ npx npm-check-updates -u
```

### secrets

```sh
VAULT_ROLE_ID=
VAULT_SECRET_ID=
```

### vault

```sh
$ vault auth enable approle
$ vault write auth/approle/role/template-go-react-role secret_id_ttl=0 token_policies=template-go-react-policy
$ vault read auth/approle/role/template-go-react-role/role-id
$ vault write -f auth/approle/role/template-go-react-role/secret-id
```
