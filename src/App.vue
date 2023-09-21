<script setup>

import { RouterView } from 'vue-router'

import boxheader from './views/boxheader.vue'
import jumbo from './views/jumbo.vue'
</script>


<template>

  <div class="container">
  <boxheader> </boxheader>
  <jumbo text_title="ยินดีต้อนรับ Beemap" ex_box="เว็บไซต์ที่รวบรวมสถานที่ท่องเที่ยว สำหรับสายดื่ม😎🍻"></jumbo>
  <RouterView/>
  </div>

</template>

<script>
export default {
  name: 'App',
};
</script>