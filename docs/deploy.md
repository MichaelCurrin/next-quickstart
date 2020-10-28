# Deploy


## Build app

Build the app for production.

```sh
$ npm run build
```

Test the output by running a server against it.

```sh
$ npm start
```


## Release

This will run checks, increment the tag version and push the new tagged commit.

```sh
$ npm version minor
```


## Deploy pipeline

This project will run checks and build steps on [GitHub Actions](https://github.com/features/actions) on every commit or push on any branch.

See the [workflow](/.github/workflows/main.yml) config file.

See results on the [Actions](https://github.com/MichaelCurrin/next-js-quickstart/actions/) tab.

### Note
> A comment on the limitation of this template project

With the current flow **nothing is persisted** after a build, so this on a CI flow and not a CD flow.

If you want to deploy your app to GitHub Pages, follow this page: [GH Pages workflow](https://github.com/MichaelCurrin/code-cookbook/blob/master/recipes/ci-cd/github-actions/workflows/node/gh-pages.md).

Or setup your app on Netlify or Vercel.
