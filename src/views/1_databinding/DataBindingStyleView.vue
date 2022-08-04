<template>
  <div>
    <div :style="style1">스타일 바인딩 : 글씨는 red, 폰트크기는 30px</div>
    <div :style="style2">스타일 바인딩 : 글씨는 green, 폰트크기는 30px</div>
    <button @click="style1.color = 'blue'">글씨 색상 변경</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      style1: {
        color: 'red',
        // style을 js에서 바꿀때 snake 표기를 -> camel로 변경해야함
        fontSize: '30px'
      },
      style2: {
        color: 'green',
        fontSize: '30px'
      }
    }
  },
  setup() {},
  created() {},
  mouted() {},
  unmounted() {},
  methods: {}
}
</script>

<style></style>
