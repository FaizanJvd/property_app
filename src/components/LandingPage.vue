<template>
  <div>
    <NavBar/>
    <div class="flex justify-center ">

      <img src="../assets/images/title.jpg" alt="title"/>
    </div>
      <CardPage/>
      <div class="p-2">
        <img src="../assets/images/avgPrice.jpg" alt="avg"/>
      </div>
      <PlanPage/>
      <div class="flex justify-center ">
        <img src="../assets/images/map.jpg" alt="avg"/>
      </div>
      <FooterPage/>
  </div>
</template>

<script setup>
import NavBar from './NavBar.vue';
import CardPage from "./CardPage.vue"
import PlanPage from './PlanPage.vue';
import FooterPage from './FooterPage.vue';
</script>

