<template>
  <div class="wrap">
    <Header/>
    <main class="main">
      
      <router-view></router-view>

    </main>
    <Footer/>
  </div>
</template>

<script setup>
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';

</script>


<style lang="scss" scoped>
.main{
  padding-top: 75px;

}
</style>