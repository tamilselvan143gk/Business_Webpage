<template>
  <section id="hero" class=" h-screen w-full">
    <div class="text-center pt-36 text-white relative">
        <div class=" leading-8">
            <p class="text-6xl font-bold h1">Powerful Digital <br> Solutions With GK</p>
            <p class="text-2xl pt-2 h2">We are team of talented digital marketers</p>
        </div>
        <div class="flex gap-5 my-10 mx-52">
            <div class="text-xl bg-border border border-gray-400 px-10 py-5">
                <i class="fa-solid fa-store text-orange-300"></i>
                <p class="cursor-pointer cursor">Lorem <br> Ipsum</p>
            </div>
            <div class="text-xl bg-border border border-gray-400 px-2 py-5">
                <i class="fa-solid fa-chart-simple text-lg px-1 text-orange-300 border-[3px] border-orange-300"></i>
                <p class="cursor-pointer cursor">Dolor Sitema</p>
            </div>
            <div class="text-xl bg-border border border-gray-400 px-5 py-5">
                <i class="fa-regular fa-calendar-check text-orange-300 text-2xl"></i>
                <p class="cursor-pointer cursor">Sedare <br> Perspiciatis</p>
            </div>
            <div class="text-xl bg-border border border-gray-400 px-8 py-5">
                <i class="fa-solid fa-paint-roller text-orange-300"></i>
                <p class="cursor-pointer cursor">Magni <br> Dolores</p>
            </div>
            <div class="text-xl bg-border border border-gray-400 px-7 py-5">
                <i class="fa-solid fa-database text-orange-300"></i>
                <p class="cursor-pointer cursor">Nemos <br> Enimade</p>
            </div>
        </div>
    </div>
  </section>
</template>

<script>
export default {
    data() {
        return {

        }
    },
}
</script>

<style>
#hero{
    background: url(../public/img/hero-bg.jpg) top center;
    background-size: cover;
    position: relative;
}
#hero:before {
    content: "";
    position: absolute;
    background: rgba(0, 0, 0, 0.6);
    bottom: 0;
    top: 0;
    left: 0;
    right: 0;
}
@media (min-width: 1024px) {
  #hero {
    background-attachment: fixed;
  }
}
@media (max-width: 768px) {
  #hero .h1 {
    font-size: 28px;
    line-height: 36px;
  }

  #hero .h2 {
    font-size: 20px;
    line-height: 24px;
  }
}
@media screen and (max-width: 768px) {
    .flex {
        flex-direction: column;
        margin: 10px;
    }

    .flex > div {
        width: 100%;
        margin-bottom: 10px;
    }
    #hero{
        height: 100%;
    }
}
.bg-border{
    transition: 0.5s;
}
.bg-border:hover{
    border: 1px solid #ffc451;
}
.cursor{
    transition: 0.5s;
}
.cursor:hover{
    color: #ffc451;
}
</style>