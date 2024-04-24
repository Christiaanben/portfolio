<template>
  <div class="info-card">
    <slot></slot>
  </div>
</template>

<script>
import {defineComponent} from 'vue'

export default defineComponent({
  name: 'InfoCard',
})
</script>

<style scoped>
.info-card {
  background-color: #f8f8f8; /* Off-white background */
  padding: 12px;            /* Padding for internal spacing */
  border-radius: 12px;      /* Rounded corners */
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Subtle shadow for depth */
  max-width: 500px;         /* Maximum width to maintain aesthetics */
  margin: 20px auto;        /* Centering in the page and providing some margin */
  box-sizing: border-box;   /* Includes padding in the width calculation */
}
</style>
