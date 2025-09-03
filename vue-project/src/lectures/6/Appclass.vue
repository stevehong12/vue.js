<template>
  <div>
    <div :class="{ active: isActive }">텍스트 입니다</div>
    <button v-on:click="toggle">toggle</button>
  </div>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    const toggle = () => {
      isActive.value = !isActive.value;
    };
    const isActive = ref(true);
    return { isActive, toggle };
  },
};
</script>

<style scoped>
.active {
  font-weight: bold;
}
</style>
