<template>
  <div class="aqsaam" id="Aqsam">
    <div class="aqsaam-header">
      <h1 class="aqsaam-title">تصفح دورات الأقسام الأكثر طلبا من عملائنا
        <div class="rectangle3"></div>
      </h1>
    </div>
    <div class="aqsaam-btn">
      <div id="btn"> </div>
      <button type="button"  class="aqsaam-btns1">دورات</button>
      <button type="button" class="aqsaam-btns2">شهادات</button>
    </div>
    <div class="Aqsam-container">
          <CardFirst  :name="المحاسبة" :id=1  />
          <CardSecond :crd="card1" />
          <CardSecond :crd="card2"/>

          <CardSecond :crd="card3"/>
          <CardSecond :crd="card4"/>
          <CardFirst :id=2 :name="الإدارة"/>


          <CardFirst :id=3 :name="التصميم"/>
          <CardSecond :crd="card5"/>
          <CardSecond :crd="card6"/>
    </div>
  </div>
</template>
<script>
import CardFirst from "~/components/CardFirst";
import CardSecond from "~/components/CardSecond";
export default {
  el:'#Aqsam',
  components:{
   CardFirst,CardSecond
  },
  data(){
    return{
      card1: [
        {imagesC:require('~/assets/images/mohasaba1.png')},
        {nameC:"مقدمة في المحاسبة"},
        {teamC:[{pic:require('~/assets/images/pepole4.png')}]},
        {nameTeamC:[{nac:"سميرةأمجد حمدي"}]},
  ],
      card2:[
        {imagesC:require('~/assets/images/mohasaba2.png')},
        { nameC:" المحاسبة الادارية"},
        {teamC:[{pic:require('~/assets/images/pepole1.png')},{pic:require('~/assets/images/pepole3.png')}]},
        {nameTeamC:[{nac:" أية جمال"},{nac:"عببسي النهار"}]},
  ],
      card3:[
        { imagesC:require('~/assets/images/dorat1.png')},
        { nameC:" إدارة المشتريات والمخازن"},
        {teamC:[{pic:require('~/assets/images/pepole2.png')},{pic:require('~/assets/images/pepole3.png')}]},
        { nameTeamC:[{nac:" سميرة مصري"},{nac:"أحمد توفيق"}]},
  ],
      card4:[
        {imagesC:require('~/assets/images/dorat2.png')},
        {nameC:"إدارة الموارد البشرية"},
        {teamC:[{pic:require('~/assets/images/pepole2.png')}]},
        { nameTeamC:[{nac:"محمد سامي"}]},
  ],
      card5:[
        {imagesC:require('~/assets/images/tasmem1.png')},
        {nameC:"تصميم المحتوى الجرافيكي"},
        { teamC:[{pic:require('~/assets/images/pepole3.png')}]},
        {nameTeamC:[{nac:"سميرة أمجد"}]},
  ],
      card6:[
        { imagesC:require('~/assets/images/tasmem2.png')},
        {nameC:"مبادئ اخلاقيات المصمم"},
        {teamC:[{pic:require('~/assets/images/pepole2.png')}]},
        {nameTeamC:[{nac:"أيمن"}]},
  ],
  }
}
}
</script>
