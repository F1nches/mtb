<template>
  <div class="about">
    <HeaderInner/>
    <PageTitle :title="title" :background="titleBackground"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HeaderInner from '@/components/HeaderInner.vue'
import PageTitle from '@/components/PageTitle.vue'

export default {
  name: 'about',
  components: {
    HeaderInner,
    PageTitle
  },
  data() {
    return {
      title: require('@/assets/page-title-about-us.svg'),
      titleBackground: require('@/assets/about-bg.jpeg')
    }
  }
}
</script>
