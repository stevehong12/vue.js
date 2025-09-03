<template>
  <div>
    <ul>
      <template v-for="(item, index) in items" :key="item.id">
        <li v-if = "item.id % 2 ===0" >
          ID : {{item.id}} 인덱스 : {{index}}, {{item.message}}
        </li>
      </template>
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