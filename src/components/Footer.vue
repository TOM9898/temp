<template>
  <div class="footer">
    <label>
      <input type="checkbox" />
    </label>
    <span><span>已完成0</span>/全部2</span>
    <button class="btn">清除已完成任务</button>
  </div>
</template>
<script lang="ts">
import { defineComponent } from "vue";
export default defineComponent({
  name: "Footer",
});
</script>
<style scoped>
</style>