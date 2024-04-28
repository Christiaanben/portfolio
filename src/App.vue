<template>
  <div class="container">
    <the-avatar
        avatar-url="profile-photo.jpg"
    />
    <div class="cards-container">
      <info-card style="grid-column: 1 / -1">
        <strong>Bennie van Eeden</strong>
        <p>Full Stack Developer</p>
      </info-card>
      <info-card style="grid-row: 2 / -1">Join Bennie's Meeting</info-card>
      <info-card>Hello! I'm in South Africa</info-card>
      <info-card style="grid-row: 3 / span 2">Their time: 21:24 SAST</info-card>
      <info-card>Schedule a meeting</info-card>
      <info-card style="grid-row: 2 / span 4; grid-column: 3">Email LinkedIn Twitter CV</info-card>
    </div>
  </div>
</template>

<script>
import TheAvatar from '@/components/TheAvatar.vue'
import InfoCard from '@/components/InfoCard.vue'

export default {
  name: 'App',
  components: {
    InfoCard,
    TheAvatar,
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: url("assets/mountainous-landscape.avif");
  background-color: rgba(0, 0, 0, 0.6);
  background-blend-mode: overlay;
  background-size: cover;
}

.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100%;
}

.cards-container {
  display: grid;
  grid-template-columns: 3fr 2fr 1fr;
  grid-template-rows: repeat(5, 10vh);
  gap: 10px; /* Adjust gap as needed */
  max-width: 960px;
  width: 80%
}

</style>
