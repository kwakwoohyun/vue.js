<template>
  <div>
    <h1>Hello {{ userName }}</h1>
    <p>message</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      userName: 'kwak',
      message: 'Vue 개발'
    }
  }
}
</script>

<style scoped></style>
