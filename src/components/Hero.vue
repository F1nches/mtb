<template>
  <div class="hero-wrapper">
    <div class="hero container-fluid" v-bind:style="{ background: 'url(' + background + ') no-repeat center center/cover'}">
      <div class="background-overlay">
        <Header/>
        <div class="header-content">
          <img v-bind:src="heroCopy"/>
        </div>
        <div class="hero-bottom">
          <img v-bind:src="heroAfter"/>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Header from '@/components/Header.vue'

export default {
  name: 'Hero',
  components: {
    Header
  },
  data() {
    return {
      background: require('@/assets/hero-bg.jpeg'),
      heroAfter: require('@/assets/hero-bottom.svg'),
      heroCopy: require('@/assets/hero-words.svg')
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hero {
  height: 900px;
  position: relative;
}

@media screen and (min-width: 1440px) {
  .hero {
    height: 1200px;
  }
}

.hero-bottom {
  bottom: 0;
  position: absolute;
  z-index: 2;
  left: 0;
  right: 0;
  bottom: -5px;
  height: 100px;
}

.hero-bottom img {
  bottom: 0;
  position: absolute;
  left: 0;
  right: 0;
}

.background-overlay {
  background: radial-gradient(rgba(255, 255, 255, 0.2),rgba(0, 0, 0, 1.0));
  position: absolute;
  left: 0;
  right: 0;
  bottom: 0;
  top: 0;
}

.header-content {
  text-align: center;
  position: absolute;
  bottom: 100px;
  width: 100%;
}

.header-content img {
  width: 80%;
  max-width: 750px;
}
</style>
