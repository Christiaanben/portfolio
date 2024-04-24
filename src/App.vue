<template>
  <div class="container">
    <the-avatar
        avatar-url="profile-photo.jpg"
    />
    <info-card>
      <p><strong>Bennie van Eeden</strong></p>
      <p>Full Stack Developer</p>
    </info-card>
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
</style>
