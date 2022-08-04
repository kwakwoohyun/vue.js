<template>
  <div>
    <div>
      <select @change="changeCity()" v-model="selectedCity" id="">
        <option value="">===옵션선택===</option>
        <option
          :value="city.cityCode"
          v-for="city in cityList"
          :key="city.cityCode"
        >
          {{ city.title }}
        </option>
      </select>
    </div>
    <div>
      <select @change="change1()" id="">
        <option
          :value="dong.dongCode"
          v-for="dong in selectedDongList"
          :key="dong.dongCode"
        >
          {{ dong.dongTitle }}
        </option>
      </select>
    </div>

    <div>
      <select @change="change1()" id="">
        <option
          :value="dong.dongCode"
          v-for="dong in dongList.filter(
            (dong) => dong.cityCode === selectedCity
          )"
          :key="dong.dongCode"
        >
          {{ dong.dongTitle }}
        </option>
      </select>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      selectedCity: '',
      cityList: [
        { cityCode: '02', title: '서울' },
        { cityCode: '031', title: '경기' },
        { cityCode: '051', title: '부산' }
      ],
      dongList: [
        { cityCode: '02', dongCode: '1', dongTitle: '구로구' },
        { cityCode: '02', dongCode: '2', dongTitle: '강동구' },
        { cityCode: '02', dongCode: '3', dongTitle: '중랑구' },
        { cityCode: '02', dongCode: '4', dongTitle: '강남구' },
        { cityCode: '051', dongCode: '1', dongTitle: '해운대구' },
        { cityCode: '051', dongCode: '2', dongTitle: '남포구' },
        { cityCode: '051', dongCode: '3', dongTitle: '부산지구' },
        { cityCode: '031', dongCode: '1', dongTitle: '구리시' },
        { cityCode: '031', dongCode: '2', dongTitle: '남양주시' },
        { cityCode: '031', dongCode: '3', dongTitle: '양주시' }
      ],
      selectedDongList: []
    }
  },
  setup() {},
  created() {},
  mouted() {},
  unmounted() {},
  methods: {
    changeCity(event) {
      console.log()
      this.selectedDongList = this.dongList.filter(
        (dong) => dong.cityCode === this.selectedCity
      )
    }
  }
}
</script>

<style></style>
