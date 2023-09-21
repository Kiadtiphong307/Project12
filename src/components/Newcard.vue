<template>

<div class="row mb-2">
        <div class="col-md-6" v-for="(n,i) in travelList" :key="n">
          <div class="row g-0 border rounded overflow-hidden flex-md-row mb-4 shadow-sm h-md-250 position-relative">
            <div class="col p-4 d-flex flex-column position-static">
              <strong class="d-inline-block mb-2 text-primary-emphasis">ร้านที่ {{ i+1 }} </strong>
              <h3 class="mb-0">{{n.name}}</h3>
              <div class="mb-1 text-body-secondary">ราคาต่อโต๊ะ {{n.price}} บาท</div>
              <p class="card-text mb-auto">{{n.text_box}}</p>
              
              <div style="margin-bottom: 30px;">
              <RouterLink :to="{name: `news_${i+1}` , params: {id: n.name}}" class="icon-link gap-1 icon-link-hover stretched-link">
               กดดูรายละเอียดเพิ่มเติม
                <svg class="bi"> <use xlink:href="#chevron-right"/></svg>
             </RouterLink>
            </div>     
            </div>
            <div class="col-auto d-none d-lg-block">
              <svg class="bd-placeholder-img" width="200" height="250" xmlns="http://www.w3.org/2000/svg" role="img"  preserveAspectRatio="xMidYMid slice" focusable="false" 
              style="margin: 15px;" >
                <image :xlink:href="n.img" x="0" y="10" width="200" height="200" />
              </svg>
            </div>
          </div>
        </div>

      
    </div>

</template>

<script setup>
import { RouterLink } from 'vue-router'
import { ref } from 'vue';



//variable drinking
const travelList=ref([
   {name: 'สุนทรารมณ์',  price:500, img:"https://media.discordapp.net/attachments/1153766321666932836/1153887346882773063/1.jpg?width=701&height=701", quantity: 0 ,
    text_box:' Let enjoy Food&Drink สุนทรารมณ์ ยินดีให้บริการ'
    }, 

  {name:'Overnight',  price:750, img:"https://media.discordapp.net/attachments/1153766321666932836/1153887347121856652/2.jpg?width=701&height=701", quantity: 0 ,
    text_box:' Overnight Bar Maejo โอเวอร์ไนท์บาร์แม่โจ ร้านย่านแม่โจ้ เชียงใหม่ มาดื่มด่ำบรรยากาศแสนชิว พร้อมเครื่องดื่ม และอาหารราคาสบายกระเป๋า มีดนตรีสดและดีเจทุกวัน'
    },
  
  {name:'Tamma Cafe',      price:1500, img:"https://media.discordapp.net/attachments/1153766321666932836/1153887347407077456/3.jpg?width=701&height=701", quantity: 0 ,
    text_box:' ตามมา คาเฟ่ ร้านของคนเก๋ คนเท่  อย่างมีสไตล์ 😎หาร้านนั่งชิลบรรยากาศดี มีดนตรีสดทั้งคืน แวะมาได้เลย ตามมา คาเฟ่ 🐵เปิดให้บริการทุกวัน'
    },

  {name:'ร้านไป-ยานใหญ่',     price:1599, img:"https://cdn.discordapp.com/attachments/1153766321666932836/1153887347616776263/4.jpg", quantity: 0 ,
    text_box:' ร้านไป-ยานใหญ่ อาหารอร่อย สะอาด ถูก ดนตรีไพเราะ บอลจอใหญ่ สังสรรค์ราคาประหยัด⚽⚽'
    },

  {name:'Too nice',    price:1699, img:"https://cdn.discordapp.com/attachments/1153766321666932836/1153887347868442642/5.png", quantity: 0 ,
    text_box:' Too Nice Nimman Enjoy our special drinks, good foods, good vibesand everyday live band at Too Nice'
    },

  {name:'ท่าช้าง คาเฟ่',  price:1890,  img:"https://cdn.discordapp.com/attachments/1153766321666932836/1153887348094943232/6.jpg", quantity: 0 ,
    text_box:' บาร์สุดคึกคักที่เสิร์ฟเครื่องดื่มและอาหารนานาชาติแบบง่ายๆ ในพื้นที่สไตล์โกดังพร้อมที่นั่งในสวน'
    },

  {name:'Beer lab',      price:675, img:"https://cdn.discordapp.com/attachments/1153766321666932836/1153887348321419314/7.jpg", quantity: 0 ,
    text_box:' We have over 250 beers from around the world and 18 beers on tap. The largest selection in Northern T'
    },

  {name:'Warm up',     price:1250, img:"https://cdn.discordapp.com/attachments/1153766321666932836/1153887346635317259/8.jpg", quantity: 0 ,
    text_box:' บาร์และสถานบันเทิงแห่งนี้มีพื้นที่หลากหลายสไตล์ให้ได้เพลิดเพลินกับดีเจที่เปิดเพลง EDM และดนตรีสด'
    },
])

</script>