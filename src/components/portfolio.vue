<template>
  <section id="portfolio" class="mx-24 mt-16">
    <div class="container">
      <div class="section-title mb-10">
        <p class="text-gray-500 tracking-widest">{{ portfolio }}</p>
        <p class="text-4xl font-bold">{{ portfolio_content }}</p>
      </div>

      <div>
        <ul id="portfolio-flters" class="flex justify-center gap-5 mb-16">
          <li
            class="cursor-pointer px-5 py-2 text-sm"
            v-for="selecter in selecters"
            :key="selecter"
            @click="selection(selecter)"
            :class="{
              'bg-orange-300 px-4 py-1 rounded-md': selected === selecter,
            }"
          >
            {{ selecter }}
          </li>
        </ul>
      </div>

      <div class="portfolio-container relative">
        <div
          class="portfolio-position absolute"
          :style="{
                top: item.top + 'px',
                left: item.left + 'px',
              }"
          v-for="item in filteredItems"
          :key="item.id"
        >
          <div class="portfolio-wrap">
            <img
              :src="item.src"
              :height="item.height"
              :width="item.width"
            />
            <div class="portfolio-info">
              <p class="text-xl text-white uppercase">{{ item.title }}</p>
              <p class="text-base text-gray-300 uppercase italic">
                {{ item.category }}
              </p>
              <div class="portfolio-links flex gap-5">
                <i class="icon port-icon ion-md-add font-bold"></i>
                <i class="icon port-icon ion-ios-link font-bold"></i>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <section class="mb-10 mx-24">
    <div class="flex gap-10">
      <div>
        <img src="../../public/img/counts-img.jpg" height="970" width="970" />
      </div>
      <div class="py-5">
        <p class="text-4xl font-semibold">
          Voluptatem dignissimos provident quasi
        </p>
        <p class="text-[14.5px] pt-5 text-gray-400">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Duis aute
          irure dolor in reprehenderit
        </p>
        <div class="grid grid-cols-2 gap-10 mt-4">
          <div class="flex gap-3">
            <div>
              <i class="icon ion-md-happy text-4xl text-orange-300"></i>
            </div>
            <div>
              <p class="text-3xl font-bold">{{ count_client }}</p>
              <p class="text-sm">
                <strong>Happy Clients</strong> consequuntur voluptas nostrum
                aliquid ipsam architecto ut
              </p>
            </div>
          </div>
          <div class="flex gap-3">
            <div>
              <i class="icon ion-ios-paper text-4xl text-orange-300"></i>
            </div>
            <div>
              <p class="text-3xl font-bold">{{ count_product }}</p>
              <p class="text-sm">
                <strong>Projects</strong> adipisci atque cum quia aspernatur
                totam laudantium et quia dere tan
              </p>
            </div>
          </div>
          <div class="flex gap-3">
            <div>
              <i class="icon ion-md-time text-4xl text-orange-300"></i>
            </div>
            <div>
              <p class="text-3xl font-bold">{{ count_years }}</p>
              <p class="text-sm">
                <strong>Years of experience</strong> aut commodi quaerat modi
                aliquam nam ducimus aut voluptate non vel
              </p>
            </div>
          </div>
          <div class="flex gap-3">
            <div>
              <i class="icon ion-md-trophy text-4xl text-orange-300"></i>
            </div>
            <div>
              <p class="text-3xl font-bold">{{ count_awards }}</p>
              <p class="text-sm">
                <strong>Awards</strong> rerum asperiores dolor alias quo
                reprehenderit eum et nemo pad der
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
  <section class="testimonials py-20 px-24">
    <div class="container">
      <div
        v-for="(testimonial, index) in testimonials"
        :key="index"
        class="mySlides fade text-center items-center text-white"
      >
        <div class="flex justify-center">
          <img
            class="block mx-auto my-0 rounded-full p-2 bg-[rgba(0,0,0,0.3)]"
            :src="testimonial.image"
            height="100"
            width="100"
          />
        </div>
        <div class="text">
          <p class="text-xl text-white font-semibold">{{ testimonial.name }}</p>
          <p class="text-sm text-gray-200">{{ testimonial.role }}</p>
          <p class="px-5 text-gray-200 italic">
            <i class="fa-solid fa-quote-left text-xl"></i>
            {{ testimonial.quote }}
            <i class="fa-solid fa-quote-right text-xl"></i>
          </p>
        </div>
      </div>
    </div>
    <div class="text-center pt-3">
      <span
        v-for="(testimonial, index) in testimonials"
        :key="index"
        @click="currentSlide(index + 1)"
        class="dot h-4 w-4 cursor-pointer my-0 mx-[2px] inline-block rounded-full bg-gray-200"
      ></span>
    </div>
  </section>
</template>

<script>
import portfolio_1 from "../../public/img/portfolio/portfolio-1.jpg";
import portfolio_2 from "../../public/img/portfolio/portfolio-2.jpg";
import portfolio_3 from "../../public/img/portfolio/portfolio-3.jpg";
import portfolio_4 from "../../public/img/portfolio/portfolio-4.jpg";
import portfolio_5 from "../../public/img/portfolio/portfolio-5.jpg";
import portfolio_6 from "../../public/img/portfolio/portfolio-6.jpg";
import portfolio_7 from "../../public/img/portfolio/portfolio-7.jpg";
import portfolio_8 from "../../public/img/portfolio/portfolio-8.jpg";
import portfolio_9 from "../../public/img/portfolio/portfolio-9.jpg";
export default {
  data() {
    return {
      portfolio: "Portfolio",
      portfolio_content: "Check our Portfolio",
      items: [
        {
          src: portfolio_1,
          title: "App",
          category: "App 1",
          height: 520,
          width: 320,
          filter: "filter-app portfolio-item",
          top: 0,
          left: 0,
        },
        {
          src: portfolio_2,
          title: "Web",
          category: "web 3",
          height: 520,
          width: 320,
          filter: "filter-web portfolio-item",
          top: 0,
          left: 350,
        },
        {
          src: portfolio_3,
          title: "App",
          category: "App 2",
          height: 520,
          width: 320,
          filter: "filter-app portfolio-item",
          top: 0,
          left: 700,
        },
        {
          src: portfolio_4,
          title: "Card",
          category: "Card 2",
          height: 520,
          width: 320,
          filter: "filter-card portfolio-item",
          top: 210,
          left: 700,
        },
        {
          src: portfolio_5,
          title: "Web",
          category: "Web 2",
          height: 520,
          width: 320,
          filter: "filter-web portfolio-item",
          top: 245,
          left: 350,
        },
        {
          src: portfolio_6,
          title: "App",
          category: "App 3",
          height: 520,
          width: 320,
          filter: "filter-app portfolio-item",
          top: 360,
          left: 0,
        },
        {
          src: portfolio_7,
          title: "Card",
          category: "Card 1",
          height: 520,
          width: 320,
          filter: "filter-card portfolio-item",
          top: 450,
          left: 700,
        },
        {
          src: portfolio_8,
          title: "Card",
          category: "Card 3",
          height: 520,
          width: 320,
          filter: "filter-card portfolio-item",
          top: 690,
          left: 700,
        },
        {
          src: portfolio_9,
          title: "Web",
          category: "Web 1",
          height: 520,
          width: 320,
          filter: "filter-web portfolio-item",
          top: 755,
          left: 350,
        },
      ],
      selecters: ["All", "App", "Card", "Web"],
      selected: "All",
      count_head: "Voluptatem dignissimos provident quasi",
      count_client: 65,
      count_product: 85,
      count_years: 35,
      count_awards: 20,
      testimonials: [
        {
          name: "Saul Goodman",
          role: "Ceo & Founder",
          quote:
            "Proin iaculis purus consequat sem cure digni ssim donec porttitora entum suscipit rhoncus. Accusantium quam, ultricies eget id, aliquam eget nibh et. Maecen aliquam, risus at semper.",
          image: "../../public/img/testimonials/testimonials-1.jpg",
        },
        {
          name: "Sara Wilsson",
          role: "Designer",
          quote:
            "Export tempor illum tamen malis malis eram quae irure esse labore quem cillum quid cillum eram malis quorum velit fore eram velit sunt aliqua noster fugiat irure amet legam anim culpa.",
          image: "../../public/img/testimonials/testimonials-2.jpg",
        },
        {
          name: "Jena Karlis",
          role: "Store Owner",
          quote:
            "Enim nisi quem export duis labore cillum quae magna enim sint quorum nulla quem veniam duis minim tempor labore quem eram duis noster aute amet eram fore quis sint minim.",
          image: "../../public/img/testimonials/testimonials-3.jpg",
        },
        {
          name: "Matt Brandon",
          role: "Freelancer",
          quote:
            "Fugiat enim eram quae cillum dolore dolor amet nulla culpa multos export minim fugiat minim velit minim dolor enim duis veniam ipsum anim magna sunt elit fore quem dolore labore illum veniam.",
          image: "../../public/img/testimonials/testimonials-4.jpg",
        },
        {
          name: "John Larson",
          role: "Entrepreneur",
          quote:
            "Quis quorum aliqua sint quem legam fore sunt eram irure aliqua veniam tempor noster veniam enim culpa labore duis sunt culpa nulla illum cillum fugiat legam esse veniam culpa fore nisi cillum quid.",
          image: "../../public/img/testimonials/testimonials-5.jpg",
        },
      ],
      slideIndex: 1,
    };
  },
  methods: {
    selection(selecters) {
      this.selected = selecters;
    },
    plusSlides(n) {
      this.showSlides(this.slideIndex += n);
    },
    currentSlide(n) {
      this.showSlides(this.slideIndex = n);
    },
    showSlides(n) {
      let i;
      let slides = document.getElementsByClassName("mySlides");
      let dots = document.getElementsByClassName("dot");
      if (n > slides.length) { this.slideIndex = 1; }
      if (n < 1) { this.slideIndex = slides.length; }
      for (i = 0; i < slides.length; i++) {
        slides[i].style.display = "none";
      }
      for (i = 0; i < dots.length; i++) {
        dots[i].className = dots[i].className.replace(" active", "");
      }
      slides[this.slideIndex - 1].style.display = "block";
      dots[this.slideIndex - 1].className += " active";
    }
  },
  mounted() {
    this.showSlides(1);
  },
  computed: {
    filteredItems() {
      if (this.selected === "All") {
        return this.items.map((item) => ({
          ...item,
          class: `img${this.items.indexOf(item) + 1}`,
        }));
      } else {
        let filteredItems = this.items.filter(
          (item) => item.title === this.selected
        );
        let counter = 0;
        return filteredItems.map((item) => {
          let imgClass = `img${counter + 1}`;
          counter++;
          return {
            ...item,
            class: imgClass,
          };
        });
      }
    },
  },
};
</script>

<style>
.portfolio-wrap {
  transition: 0.3s;
  position: relative;
  overflow: hidden;
  z-index: 1;
  background: rgba(21, 21, 21, 0.6);
}

.portfolio-wrap::before {
  content: "";
  background: rgba(21, 21, 21, 0.6);
  position: absolute;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  transition: 0.5s;
  z-index: 2;
  opacity: 0;
}

.portfolio-wrap img {
  transition: 0.5s;
}

.portfolio-wrap .portfolio-info {
  opacity: 0;
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  z-index: 3;
  transition: 0.5s;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  align-items: flex-start;
  padding: 20px;
}

.portfolio-wrap .portfolio-links {
  text-align: center;
  z-index: 4;
  color: white;
  font-size: 20px;
}

.port-icon {
  cursor: pointer;
  transition: 0.5s;
}

.port-icon:hover {
  color: #ffc451;
}

.portfolio-wrap:hover::before {
  opacity: 5;
}

.portfolio-wrap:hover img {
  transform: scale(1.2);
}

.portfolio-wrap:hover .portfolio-info {
  opacity: 1;
}

@media screen and (max-width: 768px) {
  .portfolio-container {
    margin-bottom: 20px;
  }

  .portfolio-wrap {
    width: 100%;
    margin-bottom: 20px;
  }

  .portfolio-wrap::before {
    content: "";
    background: rgba(21, 21, 21, 0.6);
    position: absolute;
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
    transition: 0.5s;
    z-index: 2;
    opacity: 0;
  }

  .portfolio-wrap img {
    width: 100%;
    transition: 0.5s;
  }

  .portfolio-wrap .portfolio-info {
    opacity: 0;
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    z-index: 3;
    transition: 0.5s;
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    align-items: flex-start;
    padding: 10px;
  }

  .portfolio-wrap .portfolio-links {
    text-align: center;
    z-index: 4;
    color: white;
    font-size: 16px;
  }

  .icon {
    cursor: pointer;
    transition: 0.5s;
  }

  .icon:hover {
    color: #ffc451;
  }

  .portfolio-wrap:hover::before {
    opacity: 5;
  }

  .portfolio-wrap:hover img {
    transform: scale(1.1);
  }

  .portfolio-wrap:hover .portfolio-info {
    opacity: 1;
  }

  .portfolio-position {
    position: static;
  }

  #portfolio {
    margin-bottom: 100px;
  }
}

.testimonials {
  background: linear-gradient(rgba(2, 2, 2, 0.5), rgba(0, 0, 0, 0.5)),
    url(public/img/testimonials-bg.jpg) fixed center center;
}
.dot {
  transition: 0.5s;
}
.active,
.dot:hover {
  background-color: yellowgreen;
}
</style>