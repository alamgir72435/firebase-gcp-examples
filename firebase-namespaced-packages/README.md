# Firebase Bundle Analysis

A look at the different ways of importing the Firebase SDK and the affect on your app's bundle size.

The accompanying [Medium Post](https://medium.com/@jthegedus/firebase-package-names-and-bundle-sizes-ec10cede63f1).

## Download

```bash
# Clone
git clone https://codeload.github.com/jthegedus/blog-examples/tar.gz/master | tar -xz --strip=2 blog-examples/firebase-namespaced-packages
cd firebase-namespaced-packages
```

## Install & Run

```bash
# Install
yarn
# Development
yarn dev
# Analyze
yarn analyze
```

## Playing with the Firebase imports

`src/index.js` is where the Firebase packages are being imported. To reproduce the results from the associated blog post, uncomment the appropriate lines:

```js
// everything
// import firebase from "firebase";

// Individual exports & core lib
// import database from "firebase/database";
// import messaging from "firebase/messaging";

// Scoped packages where core lib is explicit
// import { firebase } from "@firebase/app";
// import "@firebase/database";
// import "@firebase/messaging";
```

## Credit

This example is modified from [this Next.js example](https://github.com/zeit/next.js/tree/canary/examples/with-webpack-bundle-analyzer).