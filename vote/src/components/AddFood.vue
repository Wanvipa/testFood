<template lang="html">
  <br>
  picture : <input v-model="picture"><br><br>
  name : <input v-model="name"><br><br>
  price: <input v-model="price"><br><br>
  <button @click ="add">add</button>
</template>

<script>
export default {
  props: ['addFood'],
  data () {
    return {
      picture: '',
      name: '',
      price: ''
    }
  },
  computed: {},
  mounted () {},
  methods: {
    add: function () {
      this.addFood(this.picture, this.name, this.price)
      this.picture = ''
      this.name = ''
      this.price = ''
    }
  },
  components: {}
}
</script>

<style lang="css">
</style>
