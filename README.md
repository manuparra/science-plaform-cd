# Science Portal CD
CANFAR Science Platform Continuous Deployment with FluxCD

## Bootstrapping a new Flux CD agent on a Kubernetes Cluster

First install the FluxCD CLI within the Kubernetes Cluster you want to start with CD: 

```
curl -s https://fluxcd.io/install.sh | sudo bash
```

To bootstrap Flux for a repository owned by a personal account, you can generate a GitHub PAT that can create repositories by checking all permissions under repo.

Then you need to tun the bootstrap for this repository and specific folder, i.e. `/espSRC/production/`:

```
flux bootstrap github \
  --token-auth \
  --owner=<you_github_user> \
  --repository=science-platform-cd \
  --branch=main \
  --path=espsrc/production \
  --personal
```




