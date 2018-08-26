<template>
  <div class="hero-wrapper">
    <div class="hero container-fluid" v-bind:style="{ background: 'url(' + background + ') no-repeat center center/cover'}">
      <div class="background-overlay">
        <div class="header-content">
          <img v-bind:src="title"/>
        </div>
        <div class="hero-bottom">
          <img v-bind:src="pageTitleAfter"/>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'PageTitle',
  props: [
    "title",
    "background"
  ],
  data() {
    return {
      pageTitleAfter: require('@/assets/inner-bottom-one.svg'),
      pageTitle: require('@/assets/page-title-bike-comparison.svg')
    }
  },
  computed: {

  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hero {
  height: 300px;
  position: relative;
}

@media screen and (min-width: 1440px) {
  .hero {
    height: 500px;
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
  display: flex;
  align-items: center;
}

.header-content {
  text-align: center;
  width: 100%;
}

.header-content img {
  width: 80%;
  max-width: 750px;
}
</style>
