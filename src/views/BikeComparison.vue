<template>
  <div class="bike-comparison">
    <HeaderInner/>
    <PageTitle/>
  </div>
</template>

<script>
// @ is an alias to /src
import HeaderInner from '@/components/HeaderInner.vue'
import PageTitle from '@/components/PageTitle.vue'
import BikeComparisonChart from '@/components/BikeComparisonChart.vue'

export default {
  name: 'bikecomparison',
  components: {
    HeaderInner,
    PageTitle,
    BikeComparisonChart
  }
}
</script>
