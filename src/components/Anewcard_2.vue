<template>
    <div class="box_all">
    <div class="col" v-for="(n,i) in travelList" :key="n">
      <div class="card" style="width: 25rem;" >
        <img :src="n.img" class="card-img-top">
        <div class="card-body">
          <h3 class="card-title">{{ n.name }}</h3>
          <p>ราคาโต๊ะ : {{n.price}}</p>
          <h6>***จำกัด 5 คนต่อ 1 โต๊ะ***</h6>

          <a class="btn btn-primary" @click="list_local_control(i.name, i.quantity)"> จองโต๊ะ </a>
        </div>
      </div>
    </div>
  </div>

</template>

<script setup>

import { ref } from 'vue';

const travelList=ref([
    {name:'Overnight',  price:750, img:"https://media.discordapp.net/attachments/1153766321666932836/1153887347121856652/2.jpg?width=701&height=701", quantity: 0 ,
    text_box:' Overnight Bar Maejo โอเวอร์ไนท์บาร์แม่โจ ร้านย่านแม่โจ้ เชียงใหม่ มาดื่มด่ำบรรยากาศแสนชิว พร้อมเครื่องดื่ม และอาหารราคาสบายกระเป๋า มีดนตรีสดและดีเจทุกวัน'
    }])

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
