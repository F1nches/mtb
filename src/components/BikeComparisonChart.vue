<template>
  <div class="bike-comparison-wrapper container-fluid">
    <div class="container">
      <div class="row">

        <div class="col-md-6 bike-col bike-col-1">
          <div class="bike-img-container">
            <img src="@/assets/jeffsyal.png"/>
          </div>

          <div class="spec-row row">
            <div class="col-md-6 spec-title">
              Brand
            </div>
            <div class="col-md-6">
              {{bikeOne.brand}}
            </div>
          </div>

          <div class="spec-row row">
            <div class="col-md-6 spec-title">
              Model
            </div>
            <div class="col-md-6">
              {{bikeOne.model}}
            </div>
          </div>

          <div class="spec-row row">
            <div class="col-md-6 spec-title">
              Fork
            </div>
            <div class="col-md-6">
              {{bikeOne.fork}}
            </div>
          </div>

        </div>

        <div class="col-md-6 bike-col bike-col-2">
          <div class="bike-img-container">
            <img src="@/assets/release5c.jpg"/>
          </div>

          <div class="spec-row row">
            <div class="col-md-6 spec-title">
              Brand
            </div>
            <div class="col-md-6">
              {{bikeTwo.brand}}
            </div>
          </div>

          <div class="spec-row row">
            <div class="col-md-6 spec-title">
              Model
            </div>
            <div class="col-md-6">
              {{bikeTwo.model}}
            </div>
          </div>

          <div class="spec-row row">
            <div class="col-md-6 spec-title">
              Fork
            </div>
            <div class="col-md-6">
              {{bikeTwo.fork}}
            </div>
          </div>

        </div>

      </div>
    </div> <!-- /container -->
  </div>
</template>

<script>
export default {
  name: 'BikeComparisonChart',
  data() {
    return {
      bikeOne: {
        "brand": "YT",
        "model": "Jeffsy AL",
        "fork": "RockShox Gold 140mm"
      },
      bikeTwo: {
        "brand": "Diamondback",
        "model": "Release 5C",
        "fork": "RockShox Recon 130mm"
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.bike-comparison-wrapper {
  background: #fff;
}

.bike-col img {
  max-height: 300px;
  max-width: 100%;
}

.bike-img-container {
  width: 100%;
  text-align: center;
}

.spec-title {
  font-weight: 700;
}

.spec-row {
  max-width: 70%;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
}

</style>
