<template>
  <div>
    <!-- 클래스 이름: boolean -->
    <div :class="{ 'text-blue': isError, active: isActive }">클래스 바인딩</div>
    <div :class="class2">클래스 바인딩 : 2</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isActive: true,
      isError: false,
      class2: ['active', 'text-blue']
    }
  },
  setup() {},
  created() {},
  mouted() {},
  unmounted() {},
  methods: {}
}
</script>

<style scoped>
.active {
  background-color: greenyellow;
  font-weight: bold;
}

.text-blue {
  color: skyblue;
}
</style>
