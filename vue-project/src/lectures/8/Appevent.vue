<template>
  <div>
    <button @click="printEventInfo('hi', $event)">inline event handler</button>
  </div>
  <hr>
  <input type="text" @keyup="onKeyupHandler"/>
</template>

<script>
export default {
  setup() {
    const printEventInfo = (message, event) => {
      console.log('m',message);
      console.log('m',event.target);
      console.log('m',event.target.tagName);
    }
    const onKeyupHandler = event =>{
      console.log('event',event.key)
    }
    return {printEventInfo,onKeyupHandler}
  }
}
</script>

<style lang="scss" scoped>

</style>