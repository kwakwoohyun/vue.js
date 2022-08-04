<template>
  <div>
    <select name="" id="">
      <option value="">선택</option>
      <option :value="city.code" v-for="city in cities" :key="city.code">
        {{ city.title }}
      </option>
    </select>
  </div>
  <div>
    <table>
      <thead>
        <tr>
          <th>제품번호</th>
          <th>제품명</th>
          <th>가격</th>
          <th>주문수량</th>
          <th>합계</th>
        </tr>
      </thead>
      <tbody>
        <!-- 만약 데이터에 key로 쓸만한 값이 없을때 index를 넣어준다. -->
        <!-- <tr v-for="(drink, i) in drinkList" :key="i"></tr>  -->
        <tr v-for="drink in drinkList" :key="drink.drinkId">
          <td>{{ drink.drinkId }}</td>
          <td>{{ drink.drinkName }}</td>
          <td>{{ price }}</td>
          <td><input type="number" v-model="drink.qty" /></td>
          <td>{{ drink.price * drink.qty }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cities: [
        { title: '서울', code: '02' },
        { title: '경기', code: '031' },
        { title: '부산', code: '051' }
      ],
      drinkList: [
        {
          drinkId: '1',
          drinkName: '코카콜라',
          price: 700,
          qty: 1
        },
        {
          drinkId: '2',
          drinkName: '사이다',
          price: 500,
          qty: 1
        },
        {
          drinkId: '3',
          drinkName: '환타',
          price: 300,
          qty: 1
        },
        {
          drinkId: '4',
          drinkName: '밀키스',
          price: 600,
          qty: 1
        }
      ]
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
