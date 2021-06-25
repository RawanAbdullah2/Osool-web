<template>
  <div class="container">
      <Header/>
      <div class="home-page" >
         <NavBar />
         <div class="title">
              <h1 class="title-text">لماذا<span class="text-white mr-6">أصول؟</span>
                <div class="rectangle"></div>
              </h1>
               <p class="title-info">أصول تقدم أفضل الخدمات التدريبية والاستشارية بمنهجية علمية، والمساهمة في تأهيل وتطوير وتمكين الموارد البشرية والمؤسسات العربية
              ، من خلال مواكبة المستجدات العالمية، واختيار أفضل الخبراء أكاديميـاً ومهنيـاً </p>
                    <a href="#"><p class="btn-home"> أطلب عرضا توضيحيا</p></a>
          </div>
         <CardHome/>
      </div>
      <Sponsors/>
      <div class="Dorat">
          <h1 class="Dorat-title">الدورات القصيرة
            <div class="rectangle2"> </div>
          </h1>
          <p class="Dorat-info">أصول تقدم أفضل الخدمات التدريبية والاستشارية بمنهجية علمية، والمساهمة في تأهيل وتطوير وتمكين الموارد البشرية والمؤسسات العربية،
          من خلال مواكبة المستجدات العالمية، واختيار أفضل الخبراء أكاديميـاً ومهنيـاً</p>
          <div class="Dorat-Slider">
          <swiper/>
          <button class="dorat-btn"> تصفح كل الدورات</button>
          </div>
      </div>
      <Aqsaam/>
      <Counter/>
      <Form/>
    <div class="says">
      <div class="flex justify-center text-center pb-10">
        <h1 class="text-2xl font-bold z-30"> قالوا عن أصول ...</h1>
        <div class="rectangle6"></div>
      </div>
      <div class="mr-40 xs:mr-16 md:mr-16 lg:mr-40">
        <i class="fas fa-quote-right  fa-10x " style="color:#1c1c1c ;position:absolute ;margin-top: -50px;margin-right:-70px" ></i>
        <Says/>
      </div>
    </div>

    <div class="footer ">
      <div class="grid grid-cols-2 ">
        <img src="../assets/images/logo.png"  class="w-16 h-16 mr-5"/>
        <ul class="flex flex-wrap gap-4 mt-5 mr-96">
          <li><a href="#"><img src="../assets/images/face.png"/></a></li>
          <li><a href="#"><img src="../assets/images/twi.png"/></a></li>
          <li><a href="#"><img src="../assets/images/insta.png"/></a></li>
          <li> <a href="#"><img src="../assets/images/link.png"/> </a> </li>
        </ul>
      </div>
      <hr class="opacity-10 mt-2">
      <div class="grid grid-cols-2 -mt-8">
        <ul class="flex flex-wrap gap-4 mr-5 font-light text-white text-xs">
          <li><a href="#">خريطة الموقع</a></li>
          <li><a href="#">الخدمات</a></li>
          <li><a href="#">تواصل معنا</a></li>
        </ul>
        <h1 class="font-light text-white text-xs mr-96" >Copy right @ 2020. All rights reserved</h1>
      </div>


    </div>
  </div>
</template>


<script>
import Header from '@/components/Header'
import CardHome from '@/components/CardHome'
import NavBar from "~/components/NavBar";
import Sponsors from "~/components/Sponsors";
import swiper from "~/components/swiper";
import Aqsaam from "~/components/Aqsaam";
import Counter from "~/components/Counter";
import Form from "~/components/Form";
import Says from "~/components/Says";

export default {
  components:{
    Says,
    NavBar,
    Header,CardHome,Sponsors,swiper,Aqsaam,Counter,Form

  },
}
</script>

