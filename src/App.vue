<template>

  <div class="black-bg" v-if="modal == true">
    <div class="white-bg">
      <h4>상세페이지</h4>
      <p>상세페이지 내용</p>
      <button @click="modal = false">닫기</button>
    </div>
  </div>

  <div class="menu">
    <a v-for="(a) in menu" :key="a">{{a}}</a>
  </div>



  <div v-for="(room,i) in data" :key="room">
    <img :src="data[i].image" class="room-img">
    <h4 @click="modal = true">{{data[i].title}}</h4>
    <p>{{data[i].price}}원</p>
    <p>{{data[i].content}}</p>
  </div>


</template>

<script>

import data from './assets/data.js';

export default {
  name: 'App',
  data() {
    return {
      data : data,
      modal : false,
      count : 0,
      menu : ['Home', 'Products', 'About'],
      products : ['역삼동 원룸', '천호동원룸', '마포구원룸'],
    }
  },
  methods : {
    
  },

  components: {
  }
}
</script>

<style>
body {
  margin : 0
}
div {
  box-sizing: border-box;
}
.black-bg {
  width: 50%; height: 50%;
  background: rgba(0,0,0,0.5);
  position: fixed; padding: 20px;
}
.white-bg {
  width: 50%; background: white;
  border-radius: 8px;
  padding: 20px;
}
.room-img {
  width: 50%;
  margin-top: 40px;
}

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
