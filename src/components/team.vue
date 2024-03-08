<template>
  <section class="mx-24 my-10">
    <div>
        <p class="text-gray-400 tracking-widest">Team</p>
        <p class="text-4xl font-bold pt-1 pb-10">Check Our Team</p>
        <div class="flex gap-5">
          <div v-for="team in teams" :key="team" class="relative text-center rounded-lg shadow-lg bg-gray-200">
            <img :src="team.image" alt="team" height="300" width="300" class=" rounded-t-lg">
            <div class="absolute layer bottom-0 left-0 right-0">
              <i class="icon ion-logo-twitter text-xl px-2 mx-2  bg-gray-200 rounded-md"></i>
              <i class="icon ion-logo-facebook text-xl px-2 mx-2  bg-gray-200 rounded-md"></i>
              <i class="icon ion-logo-instagram text-xl px-2 mx-2  bg-gray-200 rounded-md"></i>
              <i class="icon ion-logo-linkedin text-xl px-2 mx-2  bg-gray-200 rounded-md"></i>
            </div>
            <p class="pt-5 font-bold text-xl">{{team.name}}</p>
            <p class="pb-5 text-xs pt-1 italic">{{team.role}}</p>
          </div>
        </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      teams:[
        {image:"../../public/img/team/team-1.jpg", name:"Walter White", role:"Chief Executive Officer"},
        {image:"../../public/img/team/team-2.jpg", name:"Sarah Jhonson", role:"Product Manager"},
        {image:"../../public/img/team/team-3.jpg", name:"William Anderson", role:"CTO"},
        {image:"../../public/img/team/team-4.jpg", name:"Amanda Jepson", role:"Accountant"},
      ]
    }
  },
}
</script>

<style>
.layer{
  opacity: 0;
  transition: 0.5s;
  padding: 200px 0 105px 0;
}
.layer:hover{
  opacity: 1;
}

.layer i{
  transition: 0.5s;
}

.layer i:hover{
  background-color: #ffc451;
}
</style>