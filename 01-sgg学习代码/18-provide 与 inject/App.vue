<template>
  <h1>provide 与 inject</h1>
  <h2>provide和inject提供依赖注入，功能类似 2.x 的provide/inject</h2>
  <h2>实现跨层级组件(祖孙)间通信</h2>
  <hr />
  <h1>父组件</h1>
  <p>当前颜色: {{ color }}</p>
  <button @click="color = 'red'">红</button>
  <button @click="color = 'yellow'">黄</button>
  <button @click="color = 'blue'">蓝</button>

  <hr />
  <Son />
</template>

<script lang="ts">
import { provide, ref } from "vue";
/* 
- provide` 和 `inject` 提供依赖注入，功能类似 2.x 的 `provide/inject
- 实现跨层级组件(祖孙)间通信
*/

import Son from "./components/son.vue";
export default {
  name: "ProvideInject",
  components: {
    Son,
  },
  setup() {
    const color = ref("red");

    provide("color", color);

    return {
      color,
    };
  },
};
</script>