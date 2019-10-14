<template>
  <div>
    <div
      v-for="(profile, i) in profiles"
      :key="i"
    >
      <LazyHydrate
        when-visible
      >
        <Profile
          :profile="profile"
        />
      </LazyHydrate>
    </div>
  </div>
</template>

<script>
import LazyHydrate from 'vue-lazy-hydration'

export default {
  name: 'Profiles',
  components: {
    LazyHydrate,
    Profile: () => import('@/components/Profile.vue')
  },
  props: {
    profiles: {
      type: Array,
      required: true
    }
  }
}
</script>
