<template>
  <div id="app">
    <transition name="slide-fade">
      <router-view/>
    </transition>
  </div>
</template>

<style>

body, html {
  width: 100%;
  height: 100%;
  overflow-x: hidden;
  color: #231F20;
}

/* #app {
  position: fixed;
  width: 100%;
  height: 100%;
  overflow-x: hidden
} */

@media (min-width: 1200px) {
  .container {
      max-width: 90% !important;
  }
}

.slide-fade-enter-active {
  transition: all .3s ease;
}
.slide-fade-leave-active {
  transition: all .8s cubic-bezier(1.0, 0.5, 0.8, 1.0);
}
.slide-fade-enter, .slide-fade-leave-to
/* .slide-fade-leave-active below version 2.1.8 */ {
  transform: translateX(10px);
  opacity: 0;
}

.about, .home, .suspension-settings, .bike-comparison {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
}

</style>
