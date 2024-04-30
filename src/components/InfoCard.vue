<template>
  <div class="info-card" v-if="href === ''">
    <slot></slot>
  </div>
  <a class="info-card" :href="href" v-else>
    <slot></slot>
  </a>
</template>

<script>
import {defineComponent} from 'vue'

export default defineComponent({
  name: 'InfoCard',
  props: {
    href: {
      optional: true,
      type: String,
      default: '',
    },
  }
})
</script>

<style scoped>
.info-card {
  background-color: #f8f8f8; /* Off-white background */
  padding: 12px;            /* Padding for internal spacing */
  border-radius: 12px;      /* Rounded corners */
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Subtle shadow for depth */
  margin: 0 auto;        /* Centering in the page and providing some margin */
  box-sizing: border-box;   /* Includes padding in the width calculation */
  width: 100%;
  overflow: hidden;
}
</style>
