<template>
  <div>
      <h2>보간법</h2>
    <p>{{message}}</p>
    <p v-once>{{message}}</p>
    <button v-on:click="message = message + '!'">Click!</button>
    <hr>
    <h2>html</h2>
    <p>{{rawHtml}}</p>
    <p v-html="rawHtml"></p>
  </div>
</template>

<script>
import {ref} from 'vue';
export default {
  setup() {
    const message = ref('안녕하세요!');
    const rawHtml =ref('<strong>안녕하세요</strong>');

    return {
      message,
      rawHtml
    };
  }
}
</script>

<style lang="scss" scoped>

</style>