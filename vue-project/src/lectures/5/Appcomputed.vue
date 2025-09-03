<template>
  <div>
    <h2>{{teacher.name}}</h2>
<!--    <p>{{teacher.lectures.length > 0 ? '있음' : '없음'}}</p>-->
    <p>{{hasLecture}}</p>
    <h2>이름</h2>
    <p>{{fullName}}</p>
  </div>
</template>

<script>
import {ref, computed, reactive} from "vue";

export default {
  setup() {
    const teacher = reactive({
      name : '짐코딩',
      lectures: [
          'html',
          'java',
          'vue3',
      ],
    });
    const firstName = ref('홍');
    const lastName = ref('성민');

    const fullName = computed({
      get(){
        return firstName.value + lastName.value;
      },
      set(value){
        [firstName.value, lastName.value] = value.split(' ');
      },
    });

    const hasLecture =computed(() => {
      return teacher.lectures.length > 0 ? '있음' : '없음'
    })
    fullName.value = '짐 코딩'


    return {
      teacher,
      hasLecture,
      fullName,
    }
  }
}
</script>

<style lang="scss" scoped>

</style>