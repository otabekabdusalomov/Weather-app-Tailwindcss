<template>
  <div class="flex flex-col min-h-screen font-bold bg-weather-primary">
    <SiteNavigation />
    <RouterView />
  </div>
</template>

<script>
import { RouterView } from 'vue-router';
import SiteNavigation from './components/SiteNavigation.vue';
  export default {
    components: {
      RouterView,
      SiteNavigation,
    },
  }
</script>

<style scoped>

</style>