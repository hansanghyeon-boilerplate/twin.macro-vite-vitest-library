vite에서 twin.macro를 사용하기 위해서는 `babel-plugin-twin` `babel-plugin-macros`가 필요하다.

`@emotion/styled` `@emtoion/react`를 사용하는데 위 babel 플러그인 두가지만 설정하면 `<div css="..." data-tw=""/>` 이런식으로 나오게된다. css속성은 `@emotion`의 기능이기 때문에

typescript 설정에서 jsxImportSource를 `@emotion/react`로 설정해줘야한다.

```json
{
  "compilerOptions": {
    "jsxImportSource": "@emotion/react"
```

참고자료

- https://github.com/ben-rogerson/babel-plugin-twin/issues/9#issuecomment-1318545946
- https://github.com/vitejs/vite-plugin-react/tree/main/packages/plugin-react