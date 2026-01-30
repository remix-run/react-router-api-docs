# react-router-api-docs

Currently, updating the docs is a manual process:

```sh
cd ../react-router
pnpm run clean && pnpm install && pnpm run build && pnpm run docs # NOT `pnpm docs`
cp -r public/dev/* ../react-router-api-docs/v7/
cd ../react-router-api-docs
git add . && git commit -m 'update the docs'
git push origin main
```
