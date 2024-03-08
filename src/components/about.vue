<template>
  <section>
    <div class="mx-24 my-16 flex gap-5">
        <div>
            <p class="text-3xl font-bold">Voluptatem dignissimos provident quasi corporis voluptates sit assumenda.</p>
            <p class=" text-sm pb-4">
                <i>
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore
                    magna aliqua.
                </i>
            </p>
            <ul class=" pb-6">
                <li class="flex pb-2 gap-2 text-[15px]"><i class="icon ion-md-done-all text-orange-400"></i> <p>Ullamco laboris nisi ut aliquip ex ea commodo consequat.</p></li>
                <li class="flex pb-2 gap-2 text-[15px]"><i class="icon ion-md-done-all text-orange-400"></i> <p>Duis aute irure dolor in reprehenderit in voluptate velit.</p></li>
                <li class="flex pb-2 gap-2 text-[15px]"><i class="icon ion-md-done-all text-orange-400"></i> <p>Ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate trideta storacalaperda mastiro dolore eu fugiat nulla pariatur.</p></li>
            </ul>
            <p>
                Ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate
                velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident
            </p>
        </div>
        <div>
            <img :src="about_src" alt="" height="1800" width="1500">
        </div>
    </div>
  </section>
  <section class="clients py-5 overflow-hidden mx-24">
    <div class="container">
        <div class="clients-slider">
            <div class="swiper-wrapper items-center">                
                <div class="swiper-slide" v-for="client in clients" :key="client">
                    <img class=" max-w-full h-auto" :src="client.src" height="80" width="80" >
                </div>
            </div>
            <div class="swiper-pagination"></div>
        </div>
    </div>
  </section>
  <section class="my-10 flex gap-8 mx-24">
    <div>
        <img :src="feature_src" height="600" width="700">
    </div>
    <div>
        <div class="flex gap-5 pb-8">
            <div>
                <i class="fa-solid fa-file-invoice pr-3 text-4xl text-orange-300"></i>
            </div>
            <div>
                <p class="text-xl text-gray-600 font-bold">Est labore ad</p>
                <p class="text-sm text-gray-400 pt-2">Consequuntur sunt aut quasi enim aliquam quae harum pariatur laboris nisi ut aliquip</p>
            </div>
        </div>
        <div class="flex gap-5 pb-8">
            <div>
                <i class="fa-solid fa-cube pr-1 text-4xl text-orange-300"></i>
            </div>
            <div>
                <p class="text-xl text-gray-600 font-bold">Harum esse qui</p>
                <p class="text-sm text-gray-400 pt-2">Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt</p>
            </div>
        </div>
        <div class="flex gap-5 pb-8">
            <div>
                <i class="fa-solid fa-images text-4xl text-orange-300"></i>
            </div>
            <div>
                <p class="text-xl text-gray-600 font-bold">Aut occaecati</p>
                <p class="text-sm text-gray-400 pt-2">Aut suscipit aut cum nemo deleniti aut omnis. Doloribus ut maiores omnis facere</p>
            </div>
        </div>
        <div class="flex gap-5">
            <div>
                <i class="fa-solid fa-shield pr-1 text-4xl text-orange-300"></i>
            </div>
            <div>
                <p class="text-xl text-gray-600 font-bold">Beatae veritatis</p>
                <p class="text-sm text-gray-400 pt-2">Expedita veritatis consequuntur nihil tempore laudantium vitae denat pacta</p>
            </div>
        </div>
    </div>
  </section>
</template>

<script>
import Swiper from 'swiper';
import 'swiper/swiper-bundle.css';
import aboutImg from "../../public/img/about.jpg";
import client1 from "../../public/img/clients/client-1.png";
import client2 from "../../public/img/clients/client-2.png";
import client3 from "../../public/img/clients/client-3.png";
import client4 from "../../public/img/clients/client-4.png";
import client5 from "../../public/img/clients/client-5.png";
import client6 from "../../public/img/clients/client-6.png";
import client7 from "../../public/img/clients/client-7.png";
import client8 from "../../public/img/clients/client-8.png";
import feature from "../../public/img/features.jpg";
export default {
    data() {
        return {
            about_src: aboutImg,
            clients:[
                {src:client1},
                {src:client2},
                {src:client3},
                {src:client4},
                {src:client5},
                {src:client6},
                {src:client7},
                {src:client8},
            ],
            swiper: null,
            feature_src:feature,
        }
    },
    mounted() {
    this.swiper = new Swiper('.clients-slider', {
      speed: 400,
      loop: true,
      autoplay: {
        delay: 5000,
        disableOnInteraction: false
      },
      slidesPerView: 'auto',
      pagination: {
        el: '.swiper-pagination',
        type: 'bullets',
        clickable: true
      },
      breakpoints: {
        320: {
          slidesPerView: 2,
          spaceBetween: 40
        },
        480: {
          slidesPerView: 3,
          spaceBetween: 60
        },
        640: {
          slidesPerView: 4,
          spaceBetween: 80
        },
        992: {
          slidesPerView: 6,
          spaceBetween: 120
        }
      }
    });
  },
  destroyed() {
    if (this.swiper) {
      this.swiper.destroy();
    }
  },
}
</script>

<style>
.swiper-slide img {
  opacity: 0.5;
  transition: 1s;
  filter: grayscale(100);
}
.swiper-slide img:hover {
  filter: none;
  opacity: 1;
}
.swiper-scrollbar {
  display: none;
}
</style>