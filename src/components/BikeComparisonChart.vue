<template>
  <div class="bike-comparison-wrapper container-fluid">

    <div class="container">

      <div class="compare-row">
        <div class="compare-input-wrapper">
          <input class="bike-one input" type="text"/>
        </div>
        <div class="compare-input-wrapper">
          <input class="bike-one input" type="text"/>
        </div>
        <div class="compare-button-wrapper">
          <div class="compare-btn" v-on:click="updateComparison">COMPARE</div>
        </div>
      </div>

      <div class="row">

        <div class="col-md-6 bike-col bike-col-1">
          <div class="bike-img-container">
            <img :src="bikeOneImage"/>
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
            <div class="fork col-md-6" data-value="1">
              {{bikeOne.fork.model}} - {{bikeOne.fork.travel}}mm
            </div>
          </div>

          <div class="spec-row row">
            <div class="col-md-6 spec-title">
              Rear Shock
            </div>
            <div class="fork col-md-6" data-value="1">
              {{bikeOne.rearShock.model}} - {{bikeOne.rearShock.travel}}mm
            </div>
          </div>

          <div class="spec-row row">
            <div class="col-md-6 spec-title">
              Handlebars
            </div>
            <div class="fork col-md-6" data-value="1">
              {{bikeOne.handlebars.model}} - {{bikeOne.handlebars.width}}mm
            </div>
          </div>

          <div class="spec-row row">
            <div class="col-md-6 spec-title">
              Rear Derailleur
            </div>
            <div class="fork col-md-6" data-value="1">
              {{bikeOne.rearDerailleur.model}} - {{bikeOne.rearDerailleur.speeds}} speed
            </div>
          </div>

          <div class="spec-row row">
            <div class="col-md-6 spec-title">
              Shifter
            </div>
            <div class="fork col-md-6" data-value="1">
              {{bikeOne.shifter}}
            </div>
          </div>

          <div class="spec-row row">
            <div class="col-md-6 spec-title">
              Cassette
            </div>
            <div class="fork col-md-6" data-value="1">
              {{bikeOne.cogset}}
            </div>
          </div>

          <div class="spec-row row">
            <div class="col-md-6 spec-title">
              Chain
            </div>
            <div class="fork col-md-6" data-value="1">
              {{bikeOne.chain}}
            </div>
          </div>

          <div class="spec-row row">
            <div class="col-md-6 spec-title">
              Wheels
            </div>
            <div class="fork col-md-6" data-value="1">
              {{bikeOne.wheels}}
            </div>
          </div>

          <div class="spec-row row">
            <div class="col-md-6 spec-title">
              Tires
            </div>
            <div class="fork col-md-6" data-value="1">
              Front: {{bikeOne.tires.front.model}} | {{bikeOne.tires.front.size}} <br> Rear: {{bikeOne.tires.rear.model}} | {{bikeOne.tires.rear.size}}
            </div>
          </div>

          <div class="spec-row row">
            <div class="col-md-6 spec-title">
              Brakes
            </div>
            <div class="fork col-md-6" data-value="1">
              {{bikeOne.brakes.model}}
            </div>
          </div>

          <div class="spec-row row">
            <div class="col-md-6 spec-title">
              Rotors
            </div>
            <div class="fork col-md-6" data-value="1">
              {{bikeOne.brakes.rotors}}
            </div>
          </div>

          <div class="spec-row row">
            <div class="col-md-6 spec-title">
              Pedals
            </div>
            <div class="fork col-md-6" data-value="1">
              {{bikeOne.pedals}}
            </div>
          </div>

          <div class="spec-row row">
            <div class="col-md-6 spec-title">
              Seatpost
            </div>
            <div class="fork col-md-6" data-value="1">
              {{bikeOne.seatpost}}
            </div>
          </div>

          <div class="spec-row row">
            <div class="col-md-6 spec-title">
              Extras
            </div>
            <div class="fork col-md-6" data-value="1">
              {{bikeOne.extras}}
            </div>
          </div>

        </div>

        <div class="col-md-6 bike-col bike-col-2">
          <div class="bike-img-container">
            <img :src="bikeTwoImage"/>
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
            <div class="fork col-md-6" data-value="1">
              {{bikeTwo.fork.model}} - {{bikeTwo.fork.travel}}mm
            </div>
          </div>

          <div class="spec-row row">
            <div class="col-md-6 spec-title">
              Rear Shock
            </div>
            <div class="fork col-md-6" data-value="1">
              {{bikeTwo.rearShock.model}} - {{bikeTwo.rearShock.travel}}mm
            </div>
          </div>

          <div class="spec-row row">
            <div class="col-md-6 spec-title">
              Handlebars
            </div>
            <div class="fork col-md-6" data-value="1">
              {{bikeTwo.handlebars.model}} - {{bikeTwo.handlebars.width}}mm
            </div>
          </div>

          <div class="spec-row row">
            <div class="col-md-6 spec-title">
              Rear Derailleur
            </div>
            <div class="fork col-md-6" data-value="1">
              {{bikeTwo.rearDerailleur.model}} - {{bikeTwo.rearDerailleur.speeds}} speed
            </div>
          </div>

          <div class="spec-row row">
            <div class="col-md-6 spec-title">
              Shifter
            </div>
            <div class="fork col-md-6" data-value="1">
              {{bikeTwo.shifter}}
            </div>
          </div>

          <div class="spec-row row">
            <div class="col-md-6 spec-title">
              Cassette
            </div>
            <div class="fork col-md-6" data-value="1">
              {{bikeTwo.cogset}}
            </div>
          </div>

          <div class="spec-row row">
            <div class="col-md-6 spec-title">
              Chain
            </div>
            <div class="fork col-md-6" data-value="1">
              {{bikeTwo.chain}}
            </div>
          </div>

          <div class="spec-row row">
            <div class="col-md-6 spec-title">
              Wheels
            </div>
            <div class="fork col-md-6" data-value="1">
              {{bikeTwo.wheels}}
            </div>
          </div>

          <div class="spec-row row">
            <div class="col-md-6 spec-title">
              Tires
            </div>
            <div class="fork col-md-6" data-value="1">
              Front: {{bikeTwo.tires.front.model}} | {{bikeTwo.tires.front.size}} <br> Rear: {{bikeTwo.tires.rear.model}} | {{bikeTwo.tires.rear.size}}
            </div>
          </div>

          <div class="spec-row row">
            <div class="col-md-6 spec-title">
              Brakes
            </div>
            <div class="fork col-md-6" data-value="1">
              {{bikeTwo.brakes.model}}
            </div>
          </div>

          <div class="spec-row row">
            <div class="col-md-6 spec-title">
              Rotors
            </div>
            <div class="fork col-md-6" data-value="1">
              {{bikeTwo.brakes.rotors}}
            </div>
          </div>

          <div class="spec-row row">
            <div class="col-md-6 spec-title">
              Pedals
            </div>
            <div class="fork col-md-6" data-value="1">
              {{bikeTwo.pedals}}
            </div>
          </div>

          <div class="spec-row row">
            <div class="col-md-6 spec-title">
              Seatpost
            </div>
            <div class="fork col-md-6" data-value="1">
              {{bikeTwo.seatpost}}
            </div>
          </div>

          <div class="spec-row row">
            <div class="col-md-6 spec-title">
              Extras
            </div>
            <div class="fork col-md-6" data-value="1">
              {{bikeTwo.extras}}
            </div>
          </div>

        </div>

      </div>
    </div> <!-- /container -->
  </div>
</template>

<script>
import emptyData from '../assets/emptybikes.json'
import data from '../assets/sample.json'

export default {
  name: 'BikeComparisonChart',
  data() {
    return {
      emptyData,
      data,
      bikeOne: {
      },
      bikeOneImage: '',
      bikeTwoImage: '',
      bikeTwo: {
      }
    }
  },
  computed: {

  },
  methods: {
    updateComparison: function() {
      this.bikeOne = this.data.bikes[0];
      this.bikeTwo = this.data.bikes[1];
      this.bikeOneImage = require('@/assets/' + this.data.bikes[0].image);
      this.bikeTwoImage = require('@/assets/' + this.data.bikes[1].image);
    }
  },
  created() {
    this.bikeOne = this.emptyData.bikes[0];
    this.bikeTwo = this.emptyData.bikes[0];
    this.bikeOneImage = require('@/assets/placeholder-image.jpg');
    this.bikeTwoImage = require('@/assets/placeholder-image.jpg');
    console.log(this.bikeTwo);
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.bike-comparison-wrapper {
  background: #fff;
  margin-bottom: 100px;
}

.bike-col {
  margin-top: 25px;
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

.compare-row {
  max-width: 90%;
  display: flex;
  justify-content: space-between;
  margin: 20px auto;
}
@media screen and (min-width: 800px) {
  .compare-row {
    max-width: 50%;
  }
}
.compare-row > div {
  display: inline-block;
  width: 34%;
}

.compare-row .compare-button-wrapper {
  width: 25%;
}

.compare-row input {
  width: 100%;
}

.compare-btn {
  background: #231F20;
  color: #fff;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100%;
  width: 100%;
  cursor: pointer;
  transition: 0.1s;
}

.compare-btn:hover {
  transition: 0.1s;
  background: #4F5C4F;
  font-weight: 700;
}

input[type="text"] {
  border: 2px solid #231F20;
  padding: 8px 12px;
}
</style>
