<template>
  <div class="bike-comparison">
    <HeaderInner/>
    <PageTitle :title="title" :background="titleBackground"/>
    <BikeComparisonChart/>
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
  },
  data() {
    return {
      title: require('@/assets/page-title-bike-comparison.svg'),
      titleBackground: require('@/assets/bikecomparison-bg.jpeg')
    }
  }
}
</script>
