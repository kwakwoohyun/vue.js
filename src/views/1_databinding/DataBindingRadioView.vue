<template>
  <div>
    <div>
      <input type="radio" id="html" value="HTML" v-model="favoriteLang" />
      <label for="html">HTML</label>
    </div>
    <div>
      <input type="radio" id="css" value="CSS" v-model="favoriteLang" />
      <label for="css">CSS</label>
    </div>
    <div>
      <input type="radio" id="js" value="JS" v-model="favoriteLang" />
      <label for="js">JSS</label>
    </div>
    <div>선택한 지역 : {{ favoriteLang }}</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      favoriteLang: ''
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
