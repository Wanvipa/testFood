<template>
<menus :foods="foods" :add-vote="addVote" :delete-food="deleteFood" ></menus>
<add-food :add-food="addFood" ></add-food>

</template>

<script>
import Menus from './components/Menus'
import AddFood from './components/AddFood'
export default {
  components: {
    Menus,
    AddFood
  },
  data () {
    return {
      foods: [{
        picture: 'http://www.chingcancook.com/detail_photo/02_20140820140603CHTM.jpg',
        name: 'ต้มยำกุ้ง',
        price: 250,
        vote: 0
      },
      {
        picture: 'http://www.chingcancook.com/detail_photo/02_20140820140603CHTM.jpg',
        name: 'ต้มยำกุ้ง',
        price: 250,
        vote: 0
      }]
    }
  },
  methods: {
    addFood: function (picture, name, price) {
      var data = {
        picture: picture,
        name: name,
        price: price,
        vote: 0
      }
      this.foods.push(data)
    },
    addVote: function (food) {
      var index = this.foods.indexOf(food)
      this.foods[index].vote ++
    },
    deleteFood: function (food) {
      var index = this.foods.indexOf(food)
      this.foods.splice(index, 1)
    }
  }
}
</script>

<style>
html {
  height: 100%;
}

body {

  align-items: center;
  justify-content: center;
  height: 100%;
}

#app {
  color: #2c3e50;
  margin-top: -100px;
  max-width: 600px;
  font-family: Source Sans Pro, Helvetica, sans-serif;
  text-align: center;
}

#app a {
  color: #42b983;
  text-decoration: none;
}

.logo {
  width: 100px;
  height: 100px
}
</style>
