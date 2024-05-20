# GitHub Action for building Defold games with Bob
- PRs to extend/improve accepted.
- The platform and architecture can be specified as inputs.
- The default platform is js-web and the default architecture is wasm-web.

## Why use it?
 - Super fast and super easy to share your work for Defold competitions (and further!)
 - Build and publish to GitHub Pages after tagging a build (or whenever!)
 - Don't have to maintain your own Bob the Builder scripting (hit the ground running!)
 - Accepts PRs if you want to improve and extend (come one, come all!)

## How do I use it?
GitHub Pages example: https://github.com/prismglue/balatro-fx/blob/main/.github/workflows/defold-build-site.yml

Look at the `inputs:` section of action.yml to see possible parameters. Check `outputs:` for the default output location.

It is strongly recommended that defold_version is provided to ensure builds are reproducible.

Example build step:

      - name: 'invoke defold-builder-simple'
        id: 'defold-build'
        uses: prismglue/defold-builder-simple@1.1.0
        with:
          project_title: "balatro-fx"
          defold_version: "1.8.0"
