<script setup lang="ts">
import { handleBackground } from '../layoutHelper'
import { computed } from 'vue'

import HeaderComponent from '../components/HeaderComponent.vue'
import FooterComponent from '../components/FooterComponent.vue'

const props = defineProps({
  background: {
    type: String,
    default: "./ign-theme/assets/fond_foret.png",
  },
})

const style = computed(() => handleBackground(props.background))
</script>

<template>
  <HeaderComponent />
  <div class="slidev-layout cover" :style="style">
    <div class="my-auto">
      <slot />
    </div>
  </div>
  <FooterComponent />
</template>
<style scoped>

.my-auto {
  background-color: white;
  color: black;
  padding: 1rem;
  border-radius: 13px;
}

</style>
