<template>
  <div class="home">
    
    <Hero/>
  </div>
</template>

<script>
// @ is an alias to /src
import Header from '@/components/Header.vue'
import Hero from '@/components/Hero.vue'

export default {
  name: 'home',
  components: {
    Header,
    Hero
  }
}
</script>
