<template>
<div>
  <div class="navbar">
    <div class="text-white" v-on:click="navside=!navside">
      <i class="fas fa-bars fa-2x border-2 border-white p-2"  ></i>
    </div>
    <ul v-show="navside">
      <li @click="isOpen1=!isOpen1" class="listnavbar"> <span class="text-red-800 font-bold">|</span> البرامج
        <i class="fas fa-caret-down"></i>
        <ul class="drop-down2" v-show="isOpen1">
          <li><a href="#">برنامج 1 </a> </li>
          <li><a href="#">برنامج 2 </a> </li>
          <li><a href="#">برنامج 3 </a> </li>
        </ul>
      </li>
      <li @click="isOpen2=!isOpen2" class="listnavbar">  <span class="text-red-800 font-bold">|</span>  التدريب <i class="fas fa-caret-down"></i>
        <ul class="drop-down2" v-show="isOpen2 ">
          <li><a href="#">تدريب 1 </a> </li>
          <li><a href="#">تدريب 2 </a> </li>
        </ul>
      </li>
      <li @click="isOpen3=!isOpen3" class="listnavbar">  <span class="text-red-800 font-bold">|</span> الشهادات <i class="fas fa-caret-down"></i>
        <ul class="drop-down2" v-show="isOpen3">
          <li><a href="#">شهادات 1 </a> </li>
          <li><a href="#">شهادات 2 </a> </li>
          <li><a href="#">شهادات 3 </a> </li>
          <li><a href="#">شهادات 4 </a> </li>
        </ul>
      </li>
      <li @click="isOpen4=!isOpen4" class="listnavbar">  <span class="text-red-800 font-bold">|</span> أصول <i class="fas fa-caret-down"></i>
        <ul class="drop-down2" v-show="isOpen4">
          <li><a href="#">أصول 1 </a> </li>
          <li><a href="#">أصول 2 </a> </li>
          <li><a href="#">أصول 3 </a> </li>
        </ul>
      </li>
    </ul>
  </div>

  <div class="nav">
    <ul class="nav-list">
      <li>  <img src="../assets/images/logo.png" /></li>
      <li @click="isOpen1=!isOpen1"> <span class="text-red-800 font-bold">|</span> البرامج
        <i class="fas fa-caret-down"></i>
         <ul class="drop-down" v-show="isOpen1">
           <li><a href="#">برنامج 1 </a> </li>
           <li><a href="#">برنامج 2 </a> </li>
           <li><a href="#">برنامج 3 </a> </li>
         </ul>
      </li>
      <li @click="isOpen2=!isOpen2">  <span class="text-red-800 font-bold">|</span>  التدريب <i class="fas fa-caret-down"></i>
        <ul class="drop-down" v-show="isOpen2 ">
          <li><a href="#">تدريب 1 </a> </li>
          <li><a href="#">تدريب 2 </a> </li>
        </ul>
      </li>
      <li @click="isOpen3=!isOpen3">  <span class="text-red-800 font-bold">|</span> الشهادات <i class="fas fa-caret-down"></i>
        <ul class="drop-down" v-show="isOpen3">
          <li><a href="#">شهادات 1 </a> </li>
          <li><a href="#">شهادات 2 </a> </li>
          <li><a href="#">شهادات 3 </a> </li>
          <li><a href="#">شهادات 4 </a> </li>
        </ul>
      </li>
      <li @click="isOpen4=!isOpen4" >  <span class="text-red-800 font-bold">|</span> أصول <i class="fas fa-caret-down"></i>
        <ul class="drop-down" v-show="isOpen4">
          <li><a href="#">أصول 1 </a> </li>
          <li><a href="#">أصول 2 </a> </li>
          <li><a href="#">أصول 3 </a> </li>
        </ul>
      </li>
    </ul>
    <div class="nav-log"> <a href="#" class="hover:text-red-800"> تسجيل الدخول </a> <span class="p-4">|</span> <a href="#" class="hover:text-red-800">إنشاء حساب </a> </div>
  </div>

</div>
</template>

<script>

export  default {

data(){
  return{
    isOpen1:false,
    isOpen2:false,
    isOpen3:false,
    isOpen4:false,
    navside:false,
  }
}

}
</script>
