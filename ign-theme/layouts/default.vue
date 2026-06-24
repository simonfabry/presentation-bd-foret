<script setup lang="ts">
import HeaderComponent from '../components/HeaderComponent.vue'
import FooterComponent from '../components/FooterComponent.vue'

</script>

<template>
  <section class="wrapper">
  <HeaderComponent />
  <div class="slidev-layout default">
    <div class="my-auto">
      <slot />
    </div>
  </div>
  <FooterComponent
      :author="$slidev.configs.author" 
      :title="$slidev.configs.title" 
      :total="$slidev.nav.slides.length" 
      :page="$page"/>
  </section>
</template>
<style scoped>

.wrapper {
  display: flex;
  flex-direction: column;
  height: 100%;
}

.wrapper>header, .wrapper>footer {
  flex-shrink: 0;
}

.slidev-layout {
  flex-shrink: 1;
}

.my-auto {
  background-color: white;
  color: black;
  padding: 1rem;
  border-radius: 13px;
}


</style>
