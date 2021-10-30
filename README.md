> Demo of `nuxt-bridge` with TypeScript

To enable TypeScript support in SFCs, declare the component definitions with `defineCompoennt` from `#app`:

```html
<script lang="ts">
import { defineComponent } from '#app'

export default defineComponent({
  ⋮ // type inference enabled
})
</script>
```

The `#app` alias is normally setup in `.nuxt/tsconfig.json`, but I found it's necessary to re-declare it in the root app's `tsconfig.json` to work in VS Code:

```json
{
  "extends": "./.nuxt/tsconfig.json",
  "compilerOptions": {
    "paths": {
      ⋮
      "#app": [
        "node_modules/@nuxt/bridge/dist/runtime/index"
      ],
    }
  }
}
```

https://stackoverflow.com/q/69716539/6277151