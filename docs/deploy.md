# Deploy


## Build app

Build the app for production to the `.next` directory.

```sh
$ npm run build
```

### Preview

Preview the prod build with a dev server. This supports hybrid pages, serving both statically generated and server-side rendered pages.

```sh
$ npm start
```

Or simply run this to handle both of the above.

```sh
$ npm run serve:prod
```

Then open the browser at:

- http://localhost:3000

### Export

Note that the default build output is not set up as static output - there no `index.html`.

Run this to run `build` and then process the existing build output as a statically generated Next site. Thanks to this [article](https://pagepro.co/blog/how-to-use-next-js-static-site-generator/).

```sh
$ npm run build:prod
```

The output can be found in `out/`. It will have an `index.html`.

This directory can be served without Node. Using Nginx, GitHub Pages or Netlify for example.


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

Or set up your app on Netlify or Vercel.
