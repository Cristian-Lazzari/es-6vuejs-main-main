<script >
export default {
  data() {
    return {
      generalmenu: 0,
    }
  },
  methods: {
    menuside() {
      if (this.generalmenu) {
        this.generalmenu = 0
      } else {
        this.generalmenu = 1
      }
      console.log(this.generalmenu)
    },

  }
}
</script>

<template>
  <div class="header">
    <div class="logo"><img src="https://grace.energy/wp-content/uploads/2022/03/grace-logo.svg" alt=""></div>
    <div class="nav">
      <div class="full-lang"><a href="#">ENGLISH</a></div>
      <div class="short-lang"><a href="#">EN</a></div>
      <div class="buy"><a href="#">BUY</a></div>
      <div class="user"><a href="#"><i class="bi bi-person"></i></a></div>
      <div class="bag"><a href="#"><i class="bi bi-bag"></i></a></div>
      <div class="menu-text"><a href="#">MENU</a></div>
      <div class="menu" @click=" menuside(generalmenu)" :class="generalmenu ? 'menuopen' : 'menuclose'"><a href="#"><i class="bi bi-list"></i></a></div>
    </div>
  </div>
  <div class="menusideopen" :class="generalmenu ? 'menusideopen' : 'menusideclose'">
    <div class="menuopen-left"></div>
    <div class="menuopen-right">Lorem ipsum dolor sit amet consectetur adipisicing elit. Vitae, qui aliquid! Molestiae necessitatibus nesciunt, quasi saepe ea, nulla itaque exercitationem adipisci aperiam neque cum impedit harum, suscipit sunt provident veritatis.</div>
  </div>
</template>

<style scoped lang="scss">
@use "../assets/styles/general.scss";

.header {
  padding: 50px 50px;
  background-color: #999B81;
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
}

.header a {
  font-size: 17px;
}
.nav {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 25px;
}

.lang a:hover {
  color: #FBED3F;
}

.buy a {
  color: black;
  background-color: #FBED3F;
  padding: 5px 10px 0px 10px;
}

.user i {
  font-size: 25px;
  display: flex;
  align-items: center;
}

.bag i {
  font-size: 20px;
  display: flex;
  align-items: center;
}

.menu i {
  font-size: 25px;
  display: flex;
  align-items: center;
}

.menuopen {
  background-color: #FBED3F;
  z-index: 1;
}

.menuclose {
  
}

.menusideopen {
  background-color: white;
  width: 100vw;
  height: 100vh;
  position: fixed;
  top: 0;
  right: 0;
  display: flex;
  // transition: display 1s linear ;
  // transition: width 1s linear 1s ;
  transition: all  linear 1s ;
}
.menusideclose {
  transition: all  linear 1s ;
  //display: none;
  width: 0;
  // transition: display 1s linear  ;
  // transition: width 1s linear 1s ;
}

.menuopen-left{
  width: 60%;
  background-color: red;
}
.menuopen-right{
  display: flex;
  align-items: center;
  width: 40%;
}
.short-lang{
  display: none;
}
@media (max-width: 870px) {
.menu-text{
  display: none;
}
.nav{
  gap: 15px;
}
.full-lang{
  display: none;
}
.short-lang{
  display: inline-block;
}
}
@media (max-width: 530px) {
  .header{
    padding: 50px 10px;
  }
}
</style>
