<template>
  <section class="mx-24 my-14">
    <div>
      <div class="mb-10">
        <p class="text-gray-400">Services</p>
        <p class="font-bold text-[40px]">Check our service</p>
      </div>
      <div class="text-center grid grid-cols-3 gap-5">
        <div class="border border-gray-300 service_card py-16">
          <i class="icon ion-logo-dribbble text-3xl bg-amber-400 px-4 py-2 rounded-lg"></i>
          <p class="pt-8 text-2xl font-bold pb-4 cursor-pointer">Lorem Ipsum</p>
          <p class="text-sm text-gray-500 px-5">Voluptatum deleniti atque corrupti quos dolores et quas molestias excepturi</p>
        </div>
        <div class="border border-gray-300 service_card py-16">
          <i class="icon ion-md-document text-3xl bg-amber-400 px-4 py-2 rounded-lg"></i>
          <p class="pt-8 text-2xl font-bold pb-4 cursor-pointer">Sed ut perspiciatis</p>
          <p class="text-sm text-gray-500 px-5">Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore</p>
        </div>
        <div class="border border-gray-300 service_card py-16">
          <i class="icon ion-ios-speedometer text-3xl bg-amber-400 px-4 py-2 rounded-lg"></i>
          <p class="pt-8 text-2xl font-bold pb-4 cursor-pointer">Magni Dolores</p>
          <p class="text-sm text-gray-500 px-5">Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia</p>
        </div>
        <div class="border border-gray-300 service_card py-16">
          <i class="icon ion-md-globe text-3xl bg-amber-400 px-4 py-2 rounded-lg"></i>
          <p class="pt-8 text-2xl font-bold pb-4 cursor-pointer">Nemo Enim</p>
          <p class="text-sm text-gray-500 px-5">At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis</p>
        </div>
        <div class="border border-gray-300 service_card py-16">
          <i class="icon ion-md-desktop text-3xl bg-amber-400 px-4 py-2 rounded-lg"></i>
          <p class="pt-8 text-2xl font-bold pb-4 cursor-pointer">Dele cardo</p>
          <p class="text-sm text-gray-500 px-6">Quis consequatur saepe eligendi voluptatem consequatur dolor consequuntur</p>
        </div>
        <div class="border border-gray-300 service_card py-[50px]">
          <i class="fa-solid fa-archway text-3xl bg-amber-400 px-4 py-3 rounded-lg"></i>
          <p class="pt-6 text-2xl font-bold pb-4 cursor-pointer">Divera don</p>
          <p class="text-sm text-gray-500 px-6">Modi nostrum vel laborum. Porro fugit error sit minus sapiente sit aspernatur</p>
        </div>
      </div>
    </div>
  </section>
  <section class=" bg-cover py-16 text-white cta">
    <div class="text-center px-24">
      <p class="text-2xl font-bold pb-2">{{ cta_head }}</p>
      <p>Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
      <button class="border-2 border-white mt-5 py-1.5 px-7 rounded-md font-semibold">{{ cta_head }}</button>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      cta_head:"Call To Action",
    }
  },
}
</script>

<style>
.service_card{
  transition: 0.5s;
}
.service_card:hover{
  border-color: white;
  box-shadow: 0 0 30px 0 rgba(0, 0, 0, 0.1);
}
.pb-4{
  transition: 0.5s;
}
.pb-4:hover{
  color: #ffc451;
}
@media (max-width: 768px) {
  .grid-cols-3 {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }
}

@media (max-width: 640px) {
  .grid-cols-3 {
    grid-template-columns: repeat(1, minmax(0, 1fr));
  }
  
}
.cta{
  background: linear-gradient(rgba(2,2,2,0.5),rgba(0,0,0,0.5)),url(public/img/cta-bg.jpg) fixed center center;
}
.border-2{
  transition: 0.5s;
}
.border-2:hover{
  background-color: #ffc451;
  color: black;
  border: 2px solid #ffc451;
}
</style>