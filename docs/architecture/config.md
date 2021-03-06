## Configuration

A small `config.js` file at the root of the project provides basic path settings. Developers are encouraged to edit the Gulp and Webpack files directly to suit their needs.

## Webpack

[Webpack](https://webpack.js.org/) does the heavy lifting of assets compilation and transformation. Webpack allows importing of Sass, images, fonts, and other assets into javascript files, bundling output files like CSS and javascript. Note the two webpack files at the root of the project:

- `webpack.particle.dev.js`: Development settings shared amongst all consuming apps.
- `webpack.particle.prod.js`: Production settings shared amongst all the consuming app.

Each app features three webpack files. Take for example, the `pl` app:

- `webpack.pl.shared.js`: Config shared by prod and dev
- `webpack.pl.prod.js`: Production-only config merged over the top of `webpack.pl.shared.js` and `webpack.particle.prod.js` (from root)
- `webpack.pl.dev.js`: Development-only config merged over the top of `webpack.pl.shared.js` and `webpack.particle.dev.js` (from root)

You are encouraged to read through all three files to understand how assets are parsed and prepared.

## Drupal theme config

The Drupal theme config is located at `apps/drupal`. Look for the usual `.info.yml`, `.libraries.yml`, and `.theme` files.

## Pattern Lab config

The Pattern Lab config file is located at `apps/pl/pattern-lab/config/config.yml`.
