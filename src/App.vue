<template>

  <div class="black-bg" v-if="모달창열림 == true">
    <div class="white-bg">
      <h4>상세페이지</h4>
      <p>상세페이지 내용</p>
    </div>
    <button @click="모달창열림 = false">닫기</button>
  </div>

  <div class="menu">
    <a v-for="a in 메뉴들" :key="a">{{ a }}</a>
  </div>
  
  <div>
    <img  src="./assets/room0.jpg" class="room-img">
    <h4 @click="모달창열림 = true">{{product[0]}}</h4>
    <p>월 50 만원</p>
    <button @click="신청수[0]++">신청</button> <span>신청수 :  {{ 신청수[0] }}</span>
  </div>
  <div>
    <img  src="./assets/room1.jpg" class="room-img">
    <h4 @click="모달창열림 = true">{{product[1]}}</h4>
    <p>월 60 만원</p>
    <button @click="신청수[1]++">신청</button> <span>신청수 :  {{ 신청수[1] }}</span>
  </div>
  <div>
    <img  src="./assets/room2.jpg" class="room-img">
    <h4 @click="모달창열림 = true">{{product[2]}}</h4>
    <p>월 70 만원</p>
    <button @click="신청수[2]++">신청</button> <span>신청수 :  {{ 신청수[2] }}</span>
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      모달창열림 : false,
      신청수 : [0,0,0],
      메뉴들 : ['Home', 'Shop', 'About'],
      product : ['역삼동 원룸', '천호동 원룸', '노원구 원룸'],
    }
  },
  methods :{
    /*increase(){
     this.신청수++
    }*/
  },

  components: {
  }
}
</script>

<style>

body {
  margin : 0
}
div{
  box-sizing: border-box;
}
.black-bg {
  width: 100%; height: 100%;
  background: rgba(0, 0, 0, 0.5);
  position: fixed; padding: 20px;
}
.white-bg {
  width: 100%; background: white;
  border-radius: 8px;
  padding: 20px;
}

.room-img {
  width: 100%;
  margin-top: 40px;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
  .menu {
    background-color: darkslateblue;
    padding: 15px;
    border-radius: 5px;
  }
  .menu a {
    color: white;
    padding: 10px;
  }
</style>