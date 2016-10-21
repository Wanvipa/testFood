<template lang="html">
 <menu :food="food" v-for="food in foods" :add-vote="addVote" :delete-food="deleteFood"></menu>

</template>

<script>
import Menu from './Menu'
export default {
  props: ['foods', 'addVote', 'deleteFood'],
  data () {
    return {}
  },
  computed: {},
  mounted () {},
  methods: {},
  components: {
    Menu
  }
}
</script>

<style lang="css">
</style>
