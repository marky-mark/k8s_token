# Info

A small kubectl command line wrapper which searches for secret token names and copies the token to the clipboard. If more than 1 result exists an error is shown asking to refine the query, 
as the purpose of this tool is to copy the token to your clipboard.

# Install via Homewbrew

```
brew tap teckro/k8s-token
brew update
brew install k8stoken
```

Now you can use `k8s-token` on your console

# Usage

```
k8s-token
	-d - The Default Dashboard query. The following parameters are set -n 'kube-system' -q 'kubernetes-dashboard-token'
	-n - The kubernetes namespace
	-q - The kubernetes secret name to query
	-h - Help
```

The result will be the below and the token is copied to your clipboard! 

```
query:
  namespace: kube-system
  query_name: kubernetes-dashboard-token
message: Token found! This is copied to your clipboard
secret_name: kubernetes-dashboard-token-wxyz
secret_token: eyJhbGciOiJSUzI1NiIsImtpZCI6IiJ9.eyJpc3fooiJrdWJlcm5ldGVzL3NlcnZpY2VhY2NvdW50Iiwia3ViZXJuZXRlcy5pbbarZXJ2aWNlYWNjb3VudC9uYW1lc3BhY2UiOiJrdWJlLXN5c3RlbSIsImt1YmVteckroZXMuaW8vc2VydmljZWFjY291bnQvc2VjcmV0Lm5hbWUiOiJrdWJlcm5ldGVzLWRhc2hib2FyZC10b2tlbi1kejRydiIsImt1YmVybmV0ZXMuaW8vc2VydmljZWFjY291bnQvc2VydmljZS1hY2NvdW50Lm5hbWUiOiJrdWJlcm5ldGVzLWRhc2hib2FyZCIsImt1YmVybmV0ZXMuaW8vc2VydmljZWFjY291bnQvc2VydmljZS1hY2NvdW50LnVpZCI6IjliMDgxOTcwLTFlM2MtMTFlOS1iNjM0LTAyNDZiZThiNmY4MiIsInN1YiI6InN5c3RlbTpzZXJ2aWNlYWNjb3VudDprdWJlLXN5c3RlbTprdWJlcm5ldGVzLWRhc2hib2FyZCJ9.FJAUhXCaZJQvP-As92LD-UWF216V_E85C9WYYZP643l2YdEwyu9bVIzVyqzT6VPVHFqqRZtYA5trpNpfA4hdFCX912lVSEK7k7A5Z5FDDCXndLDN3EgmdoaE02vxvGEyC-B30WMg3JJLZ2Y7wSDhD9vFFgBy2vgv3NZ0L_xGNJw2s7ivRmur4nbA5327V_kHhE4RWqLC2dmczWPUX5ySSEWP6i1D2Hps7X9C6FeO3dW71itevLv0_5QCM06VIFxgcAyUSteZIPAp7FQniIVvE1547tg7qWBTwUx281Gr39zpSOZdQb7G3iQcozku2TpEUc-TWb984iSJhOgDshLzLg
```
