<template>
  <div class="suspension-settings">
    <HeaderInner/>
    <PageTitle :title="title" :background="titleBackground"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HeaderInner from '@/components/HeaderInner.vue'
import PageTitle from '@/components/PageTitle.vue'
import SuspensionSettings from '@/components/SuspensionSettings.vue'

export default {
  name: 'suspensionsettings',
  components: {
    HeaderInner,
    PageTitle,
    SuspensionSettings
  },
  data() {
    return {
      title: require('@/assets/page-title-suspension-settings.svg'),
      titleBackground: require('@/assets/suspension-bg.jpeg')
    }
  }
}
</script>
