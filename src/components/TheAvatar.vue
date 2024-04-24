<template>
  <div class="avatar-container">
    <img :src="avatarUrl" alt="profile-photo">
  </div>
</template>

<script>
import {defineComponent} from 'vue'

export default defineComponent({
  name: 'TheAvatar',
  props: {
    avatarUrl: {
      type: String,
      required: true,
    }
  }
})
</script>

<style scoped>
.avatar-container img {
  width: 150px;          /* Adjust size as needed */
  height: 150px;         /* Adjust size as needed */
  border-radius: 50%;    /* Makes the image circular */
  border: 5px solid white; /* White border around the image */
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.3); /* Optional: Adds shadow for depth */
  object-fit: cover;     /* Ensures the image covers the space without distortion */
}
</style>