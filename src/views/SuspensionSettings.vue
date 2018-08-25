<template>
  <div class="suspension-settings">
    <HeaderInner/>
    <PageTitle/>
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
  }
}
</script>
