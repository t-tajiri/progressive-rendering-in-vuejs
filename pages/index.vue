<template>
  <div class="container">
    <Profiles :profiles="profiles" />
  </div>
</template>

<script>
import Profiles from '@/components/Profiles.vue'

export default {
  components: {
    Profiles
  },
  async asyncData({ $axios }) {
    const { results } = await $axios.$get('https://randomuser.me/api/?results=500')
    return { profiles: results }
  }
}
</script>

<style>
  .container {
    margin: 0 auto;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
  }
</style>
