<template>
  <div class="Second-Card"   @mouseover="isOpen=!isOpen">
    <p class="pt-28 absolute text-red-800 p-4 z-30 text-xl">دورة</p>
    <button :class="{ 'btn-card2' : isOpen==true}" class="hidden" >تصفح الدورة</button>
    <div class="Card2"></div>

    <div v-for="card in crd" >
        <img :src="card.imagesC" style="width:100%;"  />

        <div v-show="isOpen==false" class="card-info">
          <p > {{card.nameC}}</p>
          <div class="grid grid-cols-2 pt-2">
            <img  v-for="img in card.teamC" :src="img.pic" class="w-6 h-6 rounded-full" />
            <span  v-for="names in card.nameTeamC"> {{names.nac}},</span>
          </div>
        </div>

      <div v-show="isOpen==true" class="card-info2">
        <p class="relative z-50"> {{card.nameC}}</p>
        <div class="grid grid-cols-2 pt-2">
          <img  v-for="img in card.teamC" :src="img.pic" class="w-6 h-6 rounded-full z-50" />
          <span  v-for="names in card.nameTeamC"> {{names.nac}},</span>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
export default {
props:['crd'],
  data() {
    return {
      card1: {},
      card2: {},
      card3: {},
      card4: {},
      card5: {},
      card6: {},
      isOpen:false,
    }
  }
}
</script>
