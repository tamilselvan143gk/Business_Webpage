<template>
  <footer class="text-white bg-black mt-16">
    <div>
      <div>
        <div
          class="flex justify-between text-white px-20 py-10"
          style="background-color: #151515">
          <div class="">
            <p class="text-2xl font-bold pb-6">GK<span class="text-orange-300">.</span></p>
            <p class="text-sm pb-6 leading-6">
              A108 Adam Street <br />
              NY 535022, USA
            </p>
            <p class="text-sm mb-1"><strong>Phone:</strong> +91 9876543210</p>
            <p class="text-sm"><strong>Email:</strong> info@example.com</p>
            <div class="mt-4">
              <i class="icon ion-logo-twitter footer-icon cursor-pointer bg-gray-700 text-md px-3 py-1 rounded"></i>
              <i class="icon ion-logo-facebook footer-icon cursor-pointer bg-gray-700 text-md px-3 py-1 rounded ml-2"></i>
              <i class="icon ion-logo-instagram footer-icon cursor-pointer bg-gray-700 text-md px-3 py-1 rounded ml-2"></i>
              <i class="icon ion-logo-skype footer-icon cursor-pointer bg-gray-700 text-md px-3 py-1 rounded ml-2"></i>
              <i class="icon ion-logo-linkedin footer-icon cursor-pointer bg-gray-700 text-md px-3 py-1 rounded ml-2"></i>
            </div>
          </div>
          <div class="">
            <p class="font-semibold mb-4">Useful Links</p>
            <ul> 
              <li
                v-for="useful_link in useful_links"
                :key="useful_link"
                class="flex gap-2 text-sm mb-3"
              >
                <i class="icon ion-ios-arrow-forward text-orange-300"></i>
                <p class="cursor-pointer ul-text">{{ useful_link.ul }}</p>
              </li>
            </ul>
          </div>
          <div class="">
            <p class="font-semibold mb-4">Our Services</p>
            <ul>
              <li
                v-for="our_service in our_services"
                :key="our_service"
                class="flex gap-2 text-sm mb-3"
              >
                <i class="icon ion-ios-arrow-forward text-orange-300"></i>
                <p class="cursor-pointer os-text">{{ our_service.os }}</p>
              </li>
            </ul>
          </div>
          <div class="">
            <p class="font-semibold mb-4">Our Newsletter</p>
            <p class="text-sm mb-6">
              Tamen quem nulla quae legam multos aute sint culpa <br> legam noster
              magna
            </p>
            <input class="outline-none px-2 h-10 w-[250px] text-gray-500 rounded-l-lg" type="text" name="" id="" />
            <button class="px-2 py-2 bg-orange-400 submit rounded-r-lg" type="submit">
              Subscribe
            </button>
          </div>
        </div>
      </div>
      <div class="text-center py-5">
        <div>
          &copy; Copyright <strong><span>GK</span></strong
          >. All Rights Reserved
        </div>
        <div>
          <p class="text-sm">
            Designed by <a class="text-orange-400" href="https://bootstrapmade.com/">BootstrapMade</a>
          </p>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      useful_links: [
        { ul: "Home" },
        { ul: "About us" },
        { ul: "Services" },
        { ul: "Terms of service" },
        { ul: "Privacy policy" },
      ],
      our_services: [
        { os: "Web Design" },
        { os: "Web Development" },
        { os: "Product Management" },
        { os: "Marketing" },
        { os: "Graphic Design" },
      ],
    };
  },
};
</script>

<style>
.footer-icon:hover{
    background-color: #ffc451;
}
.ul-text{
    transition: 0.5s;
}
.ul-text:hover{
    color: #ffc451;
}
.os-text{
    transition: 0.5s;
}
.os-text:hover{
    color: #ffc451;
}
.submit{
    transition: 0.5s;
}
.submit:hover{
    background-color: #ffc451;
}
</style>