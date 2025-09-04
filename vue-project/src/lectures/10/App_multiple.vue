<template>
  <div></div>
</template>

<script>
import { ref, watch } from "vue";

export default {
  setup() {
    const x = ref(0);
    const y = ref(0);
    // watch(
    //   () => x.value + y.value,
    //   (sum) => {
    //     console.log("sum:", sum);
    //   }
    // );
    // 배열로 여러 값을 감시
    watch([x, y], ([newX, newY], [oldX, oldY]) => {
      console.log("x:", oldX, "->", newX);
      console.log("y:", oldY, "->", newY);
      console.log("sum:", newX + newY);
    });

    // 테스트용
    setInterval(() => {
      x.value++;
      y.value++;
    }, 1000);
    return { x, y };
  },
};
</script>

<style lang="scss" scoped></style>
