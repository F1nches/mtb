<template>
  <div class="about">
    <HeaderInner/>
  </div>
</template>

<script>
// @ is an alias to /src
import HeaderInner from '@/components/HeaderInner.vue'
import Hero from '@/components/Hero.vue'

export default {
  name: 'about',
  components: {
    HeaderInner,
    Hero
  }
}
</script>
