<template>
  <div>
    <ul>
      <li v-for = "item in items" : key="item.id">
        {{item.message}}
      </li>
    </ul>
  </div>
</template>

<script>
import {reactive} from "vue";

export default {
  setup() {
    const items =reactive([
        {id: 1, message: '1'},
        {id: 2, message: '2'},
        {id: 3, message: '3'},
        {id: 4, message: '4'},
    ])

    return {items}
  }
}
</script>

<style lang="scss" scoped>

</style>