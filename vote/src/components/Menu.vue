<template lang="html">
  <img :src="food.picture" width="200"/><br>
  name: {{food.name}}<br>
  price: {{food.price}}<br>
  vote: {{food.vote}}<br>
<button @click="addVote(food)">Vote</button>
<button @click="deleteFood(food)">X</button><br>
</template>

<script>
export default {
  props: ['food', 'addVote', 'deleteFood'],
  data () {
    return {}
  },
  computed: {},
  mounted () {},
  methods: {},
  components: {}
}
</script>

<style lang="css">
</style>
