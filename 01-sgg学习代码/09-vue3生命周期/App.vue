<template>
  <h2>App</h2>
  <button @click="isShow = !isShow">切换</button>
  <hr />
  <Child v-if="isShow" />
</template>

<script lang="ts">
import Child from "./components/child.vue";
export default {
  data() {
    return {
      isShow: true,
    };
  },

  components: {
    Child,
  },
};
</script>