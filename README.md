# Vue Lesson 20

## Memo

### `:` (shorthand for v-bind)

Use this when you want to pass a dynamic value to an attribute.

```html
<!-- Static string (no colon) -->
<my-component title="fixed text"></my-component>

<!-- JS variable or expression (with colon) -->
<my-component :title="res.title"></my-component>
<my-component :title="'Hello ' + res.title"></my-component>
<my-component :disabled="isLoading"></my-component>
```

### `v-for` and `res`

```html
<!-- "res" is a loop variable created by v-for. You can name it anything. -->
<li v-for="res in storedResources" :key="res.id">
  {{ res.title }}
</li>

<!-- "item" works the same way -->
<li v-for="item in storedResources" :key="item.id">
  {{ item.title }}
</li>
```

### `:key`

Required when rendering a list with `v-for` so Vue can identify each element.
Always pass a unique value like an ID.

```html
<learning-resource
  v-for="res in storedResources"
  :key="res.id"
></learning-resource>
```
