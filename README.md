# @k4connect/browserslist-config

## Purpose

The configuration for [browserslist](https://www.npmjs.com/package/browserslist) that we use here at K4Connect.  This provides autoconfiguration for a variety
of projects, including:
  * [`@babel/preset-env`](https://babeljs.io/docs/en/next/babel-preset-env.html) -- lets you write ESNext despite your target environment.
  * [Autoprefixer](https://github.com/postcss/autoprefixer) -- lets you forget about vendor prefixes in CSS entirely, freeing you up to use modern CSS without duplicating implementation details in multiple vendor-specific properties
  * [`postcss-normalize`](https://github.com/csstools/postcss-normalize/blob/master/README.md) -- ensures you have the minimal patches necessary to get consistent CSS behavior between target browsers
  * [`postcss-preset-env`](https://preset-env.cssdb.org/features) -- allows you to use modern CSS features (eg: ["custom properties", otherwise known as "CSS variables"](https://preset-env.cssdb.org/features#custom-properties)) while maintaining compatibility with all desired targets

## Usage

Two steps:

  1.  `npm install --save-dev @k4connect/browserslist-config`
  2.  Add this to your `package.json`:
    * If you are targetting Node: `"browerserslist": [ "extends @k4connect/browserslist-config/node.js" ]`
    * If you are targetting browsers: `"browerserslist": [ "extends @k4connect/browserslist-config/browser.js" ]`
    * If you are targetting React Native, you'll have to research how to configure `browserslist` properly and then update this repo.  Or you could just try the Node one: it'll probably work.
