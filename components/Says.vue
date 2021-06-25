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
       <swiper-slide v-for="card in Cards" :key="card.name" >
          <div class=" pb-10 p-3 w-96 my-14 z-40" style="background-color:#333333">
              <div class="flex -mt-8 mr-5">
                <img :src="card.images" class="w-14 h-14 object-cover rounded-full border-2 border-black   " />
              </div>
              <h1 class="pt-5"> "  {{card.info}}"</h1>
              <p class="text-sm font-light text-red-800 pt-10">{{ card.name }}</p>
              <p class="text-sm font-light  "> {{ card.position}}<span class="mr-3">{{ card.time }}</span></p>
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
        Cards: [
          {
            images: require('~/assets/images/say1.png'),
            info: 'كان مؤتمر المرأة منظم جدا, شمل مشاركات من الأردن و الوطن العربي',
            name: 'كارلوين فرج',
            position: 'نائب الرئيس للخدمات العربية CNN',
            time: '2019'
          },
          {
            images: require('~/assets/images/pepole3.png'),
            info: 'كانت تجربتي مع أصور متميزة, و فريق العمل لديهم مدربون جيدا على القضايا التي تؤثر على قطاع الخدمات المالية و الاقتصادية. فكانت التجربة إيجابية للغاية. مما حفزني أن ـصبح سفيراً داعماً عن الأردن و البلاد الأخرى في الشرق الأوسط',
            name: ' أليكس شانزيه',
            position: 'رئيس اتحاد المصارف الأمريكية بفلوريدا ',
            time: 'FBA'
          },
          {
            images: require('~/assets/images/say3.png'),
            info: 'كان مؤتمر المرأة تفاعليا, تم تنظيمه بشكل متميز من قبل فريق محترف للغاية, وصولا لأدق التفاصيل',
            name: 'سوزان عفانة',
            position: 'وزير السياحة و الآثار السابق في الأردن',
            time: '2019'
          },
        ],
      swiperOption: {
        breakpoints: {
          1024: {
            slidesPerView: 2.5,
            spaceBetween: 130
          },
          850: {
            slidesPerView: 2,
            spaceBetween: 120
          },
          640: {
            slidesPerView: 2,
            spaceBetween: 150
          },
          320: {
            slidesPerView: 1,
            spaceBetween: 80
          }
        },
        loop:true,
        slidesPerView: 2.5,
        spaceBetween: 80,
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
