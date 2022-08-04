<template>
  <div>
    <input type="search" v-model="searchText" @keyup="checkEnter($event)" />
    <!-- 함수없이 vue에서 enter를 눌렀는지 체크할 수 있는 함수를 제공해준다. -->
    <input type="search" v-model="searchText" @keyup.enter="doSearch()" />
    <!-- delete, down, esc, left, right, space, tab 등 주요키에 대해 이벤트를 받을 수 있다. -->
    <input type="search" v-model="searchText" @keyup.delete="doSearch()" />
    <!-- stop = event.stopPropagation(), prevent = event.preventDefault -->
    <button @click="doSearch()">조회</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      searchText: ''
    }
  },
  setup() {},
  created() {},
  mouted() {},
  unmounted() {},
  methods: {
    doSearch() {
      console.log(this.searchText)
    },
    checkEnter(event) {
      if (event.keyCode === 13) {
        this.doSearch()
      }
    }
  }
}
</script>

<style></style>
