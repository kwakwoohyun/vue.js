<template>
  <div>
    <button @click="Add1">Add1</button>
    <p>{{ counter }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      counter: 0
    }
  },
  setup() {},
  created() {},
  mouted() {},
  unmounted() {},
  methods: {
    Add1() {
      this.counter += 1
    }
  }
}
</script>

<style></style>
