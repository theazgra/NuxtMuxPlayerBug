# NuxtMuxPlayerBug

## Bug description

- This project works just fine with `@mux/mux-player@1.11.4`, but fails to run with `@mux/mux-player@1.12.1`.
- `yarn dev` fails to start completely
- `yarn build && yarn start` results in server error:

```
[8:52:36 AM]  ERROR  require() of ES Module C:\codes\git\personal\NuxtMuxPlayerBug\NuxtMuxPlayerBug\node_modules\@mux\playback-core\dist\index.cjs.js from C:\codes\git\personal\NuxtMuxPlayerBug\NuxtMuxPlayerBug\node_modules\@mux\mux-video\dist\index.cjs.js not supported.
C:\codes\git\personal\NuxtMuxPlayerBug\NuxtMuxPlayerBug\node_modules\@mux\playback-core\dist\index.cjs.js is treated as an ES module file as it is a .js file whose nearest parent package.json contains "type": "module" which declares all .js files in that package scope as ES modules.
Instead rename C:\codes\git\personal\NuxtMuxPlayerBug\NuxtMuxPlayerBug\node_modules\@mux\playback-core\dist\index.cjs.js to end in .cjs, change the requiring code to use dynamic import() which is available in all CommonJS modules, or change "type": "module" to "type": "commonjs" in C:\codes\git\personal\NuxtMuxPlayerBug\NuxtMuxPlayerBug\node_modules\@mux\playback-core\package.json to treat all .js files as CommonJS (using .mjs for all ES modules instead).


  node_modules\@mux\playback-core\dist\index.cjs.js is treated as an ES module file as it is a .js file whose nearest parent package.json contains "type": "module" which declares all .js files in that package scope as ES modules.
  Instead rename node_modules\@mux\playback-core\dist\index.cjs.js to end in .cjs, change the requiring code to use dynamic import() which is available in all CommonJS modules, or change "type": "module" to "type": "commonjs" in C:\codes\git\personal\NuxtMuxPlayerBug\NuxtMuxPlayerBug\node_modules\@mux\playback-core\package.json to treat all .js files as CommonJS (using .mjs for all ES modules instead).

  at Object.<anonymous> (node_modules\@mux\mux-video\dist\index.cjs.js:1:1862)
  at Object.<anonymous> (node_modules\@mux\mux-player\dist\index.cjs.js:915:1084)
  at node_modules\vue-server-renderer\build.prod.js:1:76653
  at Object.<anonymous> (webpack:/external "@mux/mux-player":1:0)
  at __webpack_require__ (webpack/bootstrap:25:0)
  at Module.20 (pages/index.js:34:19)
  at __webpack_require__ (webpack/bootstrap:25:0)
  at Module.21 (pages\index.vue)
  at __webpack_require__ (webpack/bootstrap:25:0)
  at async server.js:751:21
  at async Promise.all (index 0)
  at async getRouteData (.nuxt/utils.js:180:0)
  at async Promise.all (index 0)
  at async setContext (.nuxt/utils.js:266:0)
  at async createApp (.nuxt/index.js:123:0)
  at async module.exports.__webpack_exports__.default (.nuxt/server.js:84:0)
```

## Build & Run Setup

```bash
# install dependencies
$ yarn install

# serve with hot reload at localhost:3000
$ yarn dev

# build for production and launch server
$ yarn build
$ yarn start

# generate static project
$ yarn generate
```