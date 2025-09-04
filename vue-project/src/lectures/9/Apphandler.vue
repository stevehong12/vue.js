<template>
  <div>
    <div id="modifiers">
      <div @click="clickDiv">
        DIV
        <P @click="clickP">
          P
          <span @click.stop="clickSpan"> SPAN </span>
        </P>
      </div>
    </div>
    <a href="https://naver.com" @click="clickA">a영역</a>
  </div>
</template>

<script>
export default {
  setup() {
    const clickDiv = () => {
      console.log("click1");
      location.href = "https://naver.com";
    };
    const clickP = () => {
      console.log("click2");
    };
    const clickSpan = () => {
      console.log("click3");
      alert("좋아요");
    };
    const clickA = () => {
      alert("기능");
    };
    return { clickSpan, clickDiv, clickP, clickA };
  },
};
</script>

<style scoped>
#modifiers div,
#modifiers div,
#modifiers span {
  padding: 40px;
}
#modifiers div {
  background: #ccc;
}
#modifiers p {
  background: #999;
}
#modifiers span {
  background: #666;
  display: block;
}
</style>
