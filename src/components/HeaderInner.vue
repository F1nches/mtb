<template>
  <div class="nav container-fluid">
    <div class="container">
    <!-- <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div> -->
      <div class="logo">
        <router-link to="/"><img src="@/assets/mtbt-logo.svg"/></router-link>
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
  name: 'HeaderInner',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.nav {
  background: #fff;
  padding-top: 10px;
  padding-bottom: 10px;
}

.logo img {
  height: 100px;
}

.logo img:hover {
  animation: spin 0.4s;
  animation-iteration-count: 1;
  animation-timing-function: ease-in;
}

.nav > .container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.nav-wrapper a {
  color: #231F20;
  text-transform: uppercase;
  margin: 10px 20px;
}

@-moz-keyframes spin {
    from { -moz-transform: rotate(0deg); }
    to { -moz-transform: rotate(360deg); }
}
@-webkit-keyframes spin {
    from { -webkit-transform: rotate(0deg); }
    to { -webkit-transform: rotate(360deg); }
}

@keyframes spin {
    from {transform:rotate(0deg);}
    to {transform:rotate(360deg);}
}

</style>
