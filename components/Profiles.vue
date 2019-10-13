<template>
  <div>
    <ul>
      <li
        v-for="(profile, i) in profiles"
        :key="i"
      >
        <img :src="profile.picture.medium" alt="thumbnail">
        {{ profile.name.first }} {{ profile.name.last }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Profiles',
  data: () => ({
    profiles: []
  }),
  async created() {
    const { results } = await this.$axios.$get('https://randomuser.me/api/?results=100')
    this.profiles = results
  }
}
</script>

<style scoped>
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}
</style>
