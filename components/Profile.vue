<template>
  <div>
    <img :src="profile.picture.medium" alt="thumbnail">
    {{ profile.name.first }} {{ profile.name.last }}
  </div>
</template>

<script>
export default {
  name: 'Profile',
  props: {
    profile: {
      type: Object,
      required: true
    }
  }
}
</script>
