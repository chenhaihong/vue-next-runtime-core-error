# vue-next-runtime-core-error

这段代码会导致 runtime-core.esm-bundler.js 抛出错误，

```html
<pre>
  <!-- <code class="javascript" v-hljs>const a = 100;</code> -->
  <code class="javascript">const a = 100;</code>
</pre>
```

## Steps to reproduce

```shell
git clone https://github.com/chenhaihong/vue-next-runtime-core-error.git
cd vue-next-runtime-core-error
yarn install
yarn build
npx http-server ./dist
```

Visit http://127.0.0.1:8080 , u can find the error there in the console panel.

```
runtime-core.esm-bundler.js?5c40:2020 Uncaught TypeError: Cannot read property 'el' of undefined
    at cloneIfMounted (runtime-core.esm-bundler.js?5c40:2020)
    at mountChildren (runtime-core.esm-bundler.js?5c40:4178)
    at mountElement (runtime-core.esm-bundler.js?5c40:4103)
    at processElement (runtime-core.esm-bundler.js?5c40:4075)
    at patch (runtime-core.esm-bundler.js?5c40:3988)
    at mountChildren (runtime-core.esm-bundler.js?5c40:4180)
    at mountElement (runtime-core.esm-bundler.js?5c40:4103)
    at processElement (runtime-core.esm-bundler.js?5c40:4075)
    at patch (runtime-core.esm-bundler.js?5c40:3988)
    at componentEffect (runtime-core.esm-bundler.js?5c40:4493)
```

But it works well with `yarn serve`
