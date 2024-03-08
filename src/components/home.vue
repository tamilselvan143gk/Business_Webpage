<template>
  <header>
    <div class="flex justify-around fixed top-0 right-0 left-0 bg-[rgba(0,0,0,0.8)] py-3 text-white" style="z-index: 5;">
      <p class=" cursor-pointer font-bold text-3xl">GK<span class="pl-1 text-orange-300">.</span></p>
      <nav class=" text-sm font-bold">
        <div class="navbar">
          <i class="fa-solid fa-xmark fa hidden" @click="hidemenu"></i>
          <ul class="flex gap-8 pt-2">
            <li class="cursor-pointer nav">{{home}}</li>
            <li class="cursor-pointer nav">{{about}}</li>
            <li class="cursor-pointer nav">{{service}}</li>
            <li class="cursor-pointer nav">{{portfolio}}</li>
            <li class="cursor-pointer nav">{{team}}</li>
            <li class="cursor-pointer nav">{{contact}}</li>
          </ul>
        </div>
        <i class="fa-solid fa-bars hidden absolute top-0 right-0" @click="showmenu"></i>
      </nav>
      <button class="border-2 border-orange-300 px-4 py-2 get-started rounded-lg">Get Started</button>
    </div>
  </header>
  <background></background>
  <about></about>
  <service></service>
  <Portfolio></Portfolio>
  <team></team>
  <contact></contact>
  <Footer></Footer>
</template>

<script>
import background from "./background.vue";
import about from "./about.vue";
import service from "./service.vue";
import Portfolio from "./portfolio.vue";
import team from "./team.vue";
import contact from "./contact.vue";
import Footer from "./footer.vue";
export default {
    components:{
        background,
        about,
        service,
        Portfolio,
        team,
        contact,
        Footer
    },
    data() {
      return {
        home:"Home",
        about:"About",
        service:"Service",
        portfolio:"Portfolio",
        team:"Team",
        contact:"Contact",
      }
    },
    methods: {
        hidemenu() {
            const navbar = document.querySelector('.navbar');
            navbar.style.right = '-250px';
        },
        showmenu() {
            const navbar = document.querySelector('.navbar');
            navbar.style.right = '0';
        }
    }
};
</script>

<style>
.nav{
    transition: 0.5s;
}
.nav:hover{
   color: #ffc451;
}
.get-started{
    transition: 0.5s;
}
.get-started:hover{
    color: black;
    background-color: #ffc451;
}
@media screen and (max-width: 768px) {
  .flex {
    flex-direction: column; 
    align-items: center;
    padding: auto;
    margin: auto; 
  }
  .nav {
    padding: 5px 50px;
    transition: 0.5s;
  }
  .nav:hover{
   background-color: #ffc451;
   color:black
  }
  .get-started {
    margin-top: 10px;
  }
  .navbar ul li{
    display: block;
  }
  .navbar{
    position: absolute;
    background: white;
    color: black;
    height: 100vh;
    width: 200px;
    top: 0;
    right: -250px;
    text-align: left;
    z-index: 2;
    transition: 1s;
  }
  nav .fa-solid{
    display: block;
    margin: 10px;
    font-size: 20px;
    cursor: pointer;
  }
  .navbar ul{
    padding: 0px;
  }
}
</style>