# React Router API Docs

This repository contains the [Typedoc](https://typedoc.org/)-generated React Router API docs: https://api.reactrouter.com/

These docs are automatically updated nightly via the [`docs.yml`](./.github/workflows/docs.yml) workflow

If you need to update these manually, clone this resitory and the react-router repository as sibling folders, then run the following from this repo:

```sh
cd ../react-router
pnpm run clean
pnpm install
pnpm run build
pnpm run docs:typedoc
cp -r public/dev/* ../react-router-api-docs/v7/
cd ../react-router-api-docs
git add .
git commit -m 'update the docs'
git push origin main
```
