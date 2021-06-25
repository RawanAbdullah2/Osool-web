<template>
  <client-only>
    <swiper>
      <swiper-slide>
        Only loaded and rendered in browser (client)
      </swiper-slide>
    </swiper>
  </client-only>
</template>

<template>

  <swiper class="swiper" :options="swiperOption" ref="mySwiper">
    <div class="swiper-pagination" slot="pagination"></div>


    <swiper-slide v-for="card in Cards" :key="card.title">
    <div class="slider-card">
      <div class="slider-card-content">
        <img :src="card.images" class="img-card" />
        <div  class="py-2 px-4">
          <h1 class="slider-card-title">
            <a href="#">{{ card.title }}</a>
          </h1>
        </div>
        <div class="px-4 space-y-2">
          <p class="slider-card-info"> {{card.info}}</p>
        </div>
        <div class="text-white font-bold pt-8 pr-4">المحاضرون</div>
        <div class="flex flex-row">
            <div class="card-team">
              <div>
                <ul class="flex flex-col mb-6">
                  <li >
                  <img v-for="img in card.team" :src="img.pi" class="w-6 h-6 rounded-full" />
                  <span v-for="names in card.name" class="name-team"> {{names.na}}</span>
                  </li>
                </ul>
              </div>
            </div>
            <button class="btn-card"> سجل الان</button>
      </div>
      </div>
    </div>
  </swiper-slide>


  </swiper>
</template>

<script>
import { Swiper, SwiperSlide } from 'vue-awesome-swiper'

export default {
  name: 'swiper-example-centered-slides',
  title: 'Centered slides',
  components: {
    Swiper,
    SwiperSlide
  },
  data() {
    return {
      Cards:[
        {images:require('~/assets/images/dorat1.png'),
          title:'الاقتصاد والتنمية',
          info:'دورة الاقتصاد و التنمية تتحدث عن دور الاقتصاد برفع لخدمات التدريبية والاستشارية بمنهجية علمية، والمساهمة في تأهيل وتطوير وتمكين الموارد البشرية والمؤسسات العربية',
          team:[{pi:require('~/assets/images/pepole1.png')},
            {pi:require('~/assets/images/pepole3.png')},
            {pi:require('~/assets/images/pepole2.png')}],
          name:[{na:'اية جمال'},{na:'عيسى النهار'},{na:'محمود عيسى'}]
        },
        {images:require('~/assets/images/dorat2.png'),
          title:' إداؤة المشتريات والمخازن',
          info:'دورة الاقتصاد و التنمية تتحدث عن دور الاقتصاد برفع لخدمات التدريبية والاستشارية بمنهجية علمية، والمساهمة في تأهيل وتطوير وتمكين الموارد البشرية والمؤسسات العربية',
          team:[{pi:require('~/assets/images/pepole4.png')}],
          name:[{na:' سعيد خالد'}]
        },
        {images:require('~/assets/images/dorat3.png'),
          title:'إدارة الذات والتطيور الوظيفي',
          info:'دورة الاقتصاد و التنمية تتحدث عن دور الاقتصاد برفع لخدمات التدريبية والاستشارية بمنهجية علمية، والمساهمة في تأهيل وتطوير وتمكين الموارد البشرية والمؤسسات العربية',
          team:[{pi:require('~/assets/images/pepole1.png')},{pi:require('~/assets/images/pepole3.png')},{pi:require('~/assets/images/pepole2.png')}],
          name:[{na:'اية جمال'},{na:'عيسى النهار'},{na:'محمود عيسى'}]
        },
        {images:require('~/assets/images/dorat4.png'),
          title:'الاقتصاد',
          info:"دورة الاقتصاد و التنمية تتحدث عن دور الاقتصاد برفع لخدمات التدريبية والاستشارية بمنهجية علمية، والمساهمة في تأهيل وتطوير وتمكين الموارد البشرية والمؤسسات العربية",
          team:[{pi:require('~/assets/images/pepole1.png')}],
          name:[{na:'اية جمال'}]
        }
      ],
      swiperOption: {
        breakpoints: {
          1024: {
            slidesPerView: 3.5,
            spaceBetween: 0
          },
          850: {
            slidesPerView: 2.5,
            spaceBetween: 120
          },
          768: {
            slidesPerView: 2,
            spaceBetween: 5
          },
          640: {
            slidesPerView: 1.5,
            spaceBetween: 0
          },
          320: {
            slidesPerView: 1,
            spaceBetween: 5
          }
        },
        loop:true,
        slidesPerView: 3.5,
        spaceBetween: 10,
        centeredSlides: false,
        pagination: {
          el: '.swiper-pagination',
          type: 'fraction'
        },
      }
    }
  }
}
</script>


