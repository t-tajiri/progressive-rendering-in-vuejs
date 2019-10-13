<template>
  <div class="container">
    <Profiles />
  </div>
</template>

<script>
import Profiles from '@/components/Profiles.vue'

export default {
  components: {
    Profiles
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
