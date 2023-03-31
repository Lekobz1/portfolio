<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Footer from '@/components/FooTer.vue';
import NavBar from './components/NavBar.vue';

</script>

<template>
  <header>
    <NavBar>

    </NavBar>
  </header>
  
  
    <RouterView />
  

  
    <Footer>

    </Footer>
 

  
</template>

