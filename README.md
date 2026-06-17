# React Router API Docs

This repository contains the [Typedoc](https://typedoc.org/)-generated React
Router API docs: https://api.reactrouter.com/

These docs are automatically synced from `remix-run/react-router` nightly via
the [`Update API Documentation`](./.github/workflows/docs.yml) workflow. The
workflow can also be run manually with `workflow_dispatch`.

The generated docs are written to the folder matching the major version from
`packages/react-router/package.json` in the checked-out React Router repo:

- `v7/` for React Router 7.x
- `v8/` for React Router 8.x

If you need to update these manually, clone this repository and the React Router
repository as sibling folders, then run the following (using the correct version
folder name):

```sh
cd ../react-router
pnpm run clean
pnpm install
pnpm run build
pnpm run docs:typedoc
mkdir -p "../react-router-api-docs/v8"
cp -r public/dev/* "../react-router-api-docs/v8/"
cd ../react-router-api-docs
git add .
git commit -m 'update the docs'
git push origin main
```
