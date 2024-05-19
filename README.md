# vue3-vuetify3-mastering

target:
- Mastering vue3 and API composition

project build with the following command line

```bash
npx create-vue@latest .
```
This template should help get you started developing with Vue 3 in Vite.

## Recommended IDE Setup

[VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (and disable Vetur).

## Customize configuration

See [Vite Configuration Reference](https://vitejs.dev/config/).

## Project Setup

```sh
npm install
```

### Compile and Hot-Reload for Development

```sh
npm run dev
```

### Compile and Minify for Production

```sh
npm run build
```


### Nice to know

when using <b>scoped</b> attr this help to target only the current component with css
```ts
<script scoped>

</script>
```
<b>Pinia</b> is a state manager, intuitive store for vueJS used for lager applications

<b>Option API</b> used to dynamically inject data
exemple
```ts
<script>
  export default {
    data() {
      return {
        transactions: [
          { id:1, text: 'Flower', amount: -19.99}
        ],
        name:...,
        anotherObject:...
      }
    },
    methods: newFunction();
  }
</script>
```

<b>Composition API</b> less code to write

fist way exemple

```ts
<script setup>
   const transactions = [
      { id: 1, text: 'Flower', amount: -19.99 },
      { id: 2, text: 'Salary', amount: 299.97 }
    ]
</script>
```
second way exemple

```ts
<script>
  export default {
    setup() {
      const transactions = [
          { id:1, text: 'Flower', amount: -19.99}
          { id:2, text: 'salary', amount: 2000}
        ];
      return {
        transactions,
        }
    },
  };
</script>
```
How to use data (transactionList for instance) within another component using Composition API
```ts
<script setup>
  import {defineProps} from 'vue';
  const props = defineProps({
    transactions:{
      typ: Array,
      required: true,
    }
  })
</script>
```
