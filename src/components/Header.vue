<template>
  <div class="nav container-fluid">
    <div class="container">
    <!-- <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div> -->
      <div class="logo">
        <img src="@/assets/mtbt-logo-white.svg"/>
      </div>
      <div class="nav-wrapper">
        <router-link to="/">Home</router-link>
        <router-link to="/compare">Bike Comparison</router-link>
        <router-link to="/suspension">Suspension Settings</router-link>
        <router-link to="/about">About</router-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.nav {
  background: none;
  padding-top: 10px;
  padding-bottom: 10px;
}

.logo img {
  height: 100px;
}

.nav > .container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.nav-wrapper a {
  color: #fff;
  text-transform: uppercase;
  margin: 10px 20px;
}

</style>
