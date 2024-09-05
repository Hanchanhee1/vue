<template>

  <div class="menu">
    <a v-for="(a) in menu" :key="a">{{a}}</a>
  </div>

  <div>
    <h4 v-for="(name,i) in products" :key="name">{{products[i]}}</h4>
    <p>70 만원</p>
  </div>
  <div>
    <h4 class="red" :style="style">{{products[0]}}</h4>
    <p>50 만원</p>
  </div>
  <div>
    <h4>{{products[1]}}</h4>
    <p>70 만원</p>
  </div>
  <div>
    <h4>{{products[2]}}</h4>
    <p>90 만원</p>
  </div>

</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      menu : ['Home', 'Products', 'About'],
      products : ['역삼동 원룸', '천호동원룸', '마포구원룸'],
    }
  },
  components: {
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.menu {
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}
.menu a {
  color: white;
  padding: 10px;
}

</style>
