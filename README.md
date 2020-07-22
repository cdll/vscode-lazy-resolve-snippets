## lazyResolve Snippets

Quickly and easily generate timeout/interval promise resolve in `javascript`/`typescript`/`coffeescript`.

When coding `javascript` with
```js
new Promise...
```
```js
// with timeouter
new Promise((resolve, reject) => {
  setTimeout(() => {
    if (SOME_RESOLVE_CONDITIONS) resolve()
    else reject()
  }, 0)
})
// with interval
new Promise((resolve, reject) => {
  const LOOP = setInterval(() => {
    if (SOME_RESOLVE_CONDITIONS) {
      clearInterval(LOOP)
      resolve()
    }
    else if (SOME_REJECT_REASONS) {
      clearInterval(LOOP)
      reject()
    }
    else // todos...
  }, 0)
})
```
in `typescript` is the same as the `javascript` version.

Or when coding with `coffeescript`, when
```coffee
new Promise...
```
```coffee
# with timeouter
new Promise (resolve, reject)=>
  setTimeout ()=>
    if SOME_RESOLVE_CONDITIONS
    then resolve()
    else reject()
  , 0
# with interval
new Promise (resolve, reject)=>
  LOOP = setInterval ()=>
    if SOME_RESOLVE_CONDITIONS
      clearInterval LOOP
      resolve()
    else if SOME_REJECT_REASONS
      clearInterval LOOP
      reject()
    else # todos...
  , 0
```

For any question or suggestions, pls issue me @ [repo](https://github.com/cdll/vscode-lazy-resolve-snippets/issues).