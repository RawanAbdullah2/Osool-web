<template>
<div class="First-Card">
<h1 class="first-id"> 0{{id}}</h1>
  <p  class="first-info" style="margin-top: -80px"><span class=" border-b-2 border-red-800"> قسم</span> <span>{{ name }}</span> </p>
</div>
</template>

<script>

export default {
 props:{
 id:{
    type:Number,
    required: true
 },
   name:{
    type:undefined,
     required: true

   },
 },

}
</script>
