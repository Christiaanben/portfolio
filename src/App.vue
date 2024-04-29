<template>
  <div class="container">
    <the-avatar
        avatar-url="profile-photo.jpg"
    />
    <div class="cards-container">
      <info-card class="identity-card">
        <div>
          <b>Bennie van Eeden</b>
          <div>Full Stack Developer</div>
        </div>
        <div>rather.chat</div>
      </info-card>
      <info-card style="grid-row: 2 / -1">Join Bennie's Meeting</info-card>
      <info-card>Hello! I'm in South Africa</info-card>
      <info-card style="grid-row: 3 / span 2">Their time: 21:24 SAST</info-card>
      <info-card>Schedule a meeting</info-card>
      <info-card class="contact-cards-container">
        <info-card>
          <img alt="Email" src="icons/email.png">
        </info-card>
        <a href="https://www.linkedin.com/in/bennie-van-eeden-22654a112/">
          <info-card>
            <img alt="LinkedIn" src="icons/linkedin.svg">
          </info-card>
        </a>
        <info-card>
          <img alt="Twitter" src="icons/twitter.svg">
        </info-card>
        <info-card>
          <img alt="CV" src="icons/cv.png">
        </info-card>
      </info-card>
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

.identity-card {
  grid-column: 1 / -1;

  display: flex;
  align-items: center;
  justify-content: space-between;
}

.contact-cards-container {
  grid-row: 2 / span 4;
  grid-column: 3;

  display: grid;
  grid-template-rows: repeat(4, 1fr);
  gap: 10px;
  background-color: #e0e0e0 !important;
}

.info-card img {
  max-width: 100%; /* ensures the image is not wider than the card */
  max-height: 100%; /* ensures the image is not taller than the card */
  object-fit: contain; /* scales the image to be as large as possible within the given dimension, maintaining aspect ratio */
  display: block; /* removes extra space below the image */
}

a .info-card:hover {
  background-color: #f0f0f0;
  opacity: 0.9;
}

</style>
