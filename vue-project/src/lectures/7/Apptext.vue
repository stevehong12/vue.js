<template>
  <div>
    <P v-text ="msg"></P>
    <P v-html ="htmlStr"></P>
    <P v-text ="htmlStr"></P>
  </div>
</template>

<script>
import {ref} from "vue";

export default {
  setup() {
    const msg = ref('안녕')
    const htmlStr = ref('<strong>안녕!!!</strong>')
    return {msg,htmlStr}
  }
}
</script>

<style lang="scss" scoped>

</style>