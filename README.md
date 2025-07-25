## How the setup is done

- Created the `npx-cicd-project` (which have docker credentials and PAT for *gitops-argocd-k8s* repo) repo and added `.github/workflows` deployment file which will do the following steps:
  - Checkout code
  - Docker Login
  - Build Setup
  - Set short commit (7 chars)
  - Build and Push docker image to docker hub
  - Update the `deployment.yaml` inside `gitops-argocd-k8s/npx-app-manifest` repository with latest docker image (This repo is configured with argocd on k8s cluster which will automatically detects the change and deploys the latest app to k8s cluster)

# next js app commands

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```
Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

