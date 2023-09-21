<template>
    <div class="box_all">
    <div class="col" v-for="(n,i) in travelList" :key="n">
      <div class="card" style="width: 25rem;" >
        <img :src="n.img" class="card-img-top">
        <div class="card-body">
          <h3 class="card-title">{{ n.name }}</h3>
          <p>ราคาโต๊ะ : {{n.price}}</p>
          <h6>*** จำกัด 5 คนต่อ 1 โต๊ะ ***</h6>

          <a class="btn btn-primary" @click="list_local_control(i.name, i.quantity)"> จองโต๊ะ </a>
        </div>
      </div>
    </div>
  </div>

</template>

<script setup>

import { ref } from 'vue';


const travelList=ref([
    {name:'Warm up',     price:1250, img:"https://cdn.discordapp.com/attachments/1153766321666932836/1153887346635317259/8.jpg", quantity: 0 ,
    text_box:' บาร์และสถานบันเทิงแห่งนี้มีพื้นที่หลากหลายสไตล์ให้ได้เพลิดเพลินกับดีเจที่เปิดเพลง EDM และดนตรีสด'
    },])


</script>

<style>

.card-img-top{
height: 100%;
padding: 25px;

}
.box_all{
justify-content: center;
align-items: center;
margin-left: 30%;
text-align: center
}

</style>
