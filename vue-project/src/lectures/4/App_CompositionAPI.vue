<template>
  <div >
    <h1>{{ reactiveMessage }}</h1>
    <button v-on:click="addReactiveMessage">Add m</button>
    <h2>{{normalMessage}}</h2>
    <button v-on:click ="addNormalMessage">Add m</button>
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  setup() {
    const reactiveMessage = ref('Hello Vue 3!');
    const addReactiveMessage = ()=>{
      reactiveMessage.value = reactiveMessage.value + '!';
    };

    let normalMessage = 'hello';
    const addNormalMessage =() => {
      normalMessage = normalMessage + '!'
    };
    return {
      reactiveMessage,
      normalMessage,
      addNormalMessage,
      addReactiveMessage,
    }
  }
}
</script>

<style scoped>
</style>
