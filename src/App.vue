<script setup lang="ts">
import TheSidebar from "@/components/TheSidebar.vue";
import { useStepStore } from "@/stores/step";

const stepStore = useStepStore();
</script>

<template>
  <main class="main">
    <div class="main-container">
      <TheSidebar />
      <KeepAlive>
        <component :is="`${stepStore.activeStep}`" />
      </KeepAlive>
    </div>
  </main>
  <!-- Attribution -->
 
</template>

<style scoped>
header {
  line-height: 1.5;
}

@media screen and (max-width: 47.9375rem) {
  .main {
    margin-bottom: 80px;
  }

  footer {
    margin-bottom: 120px;
  }
}
</style>
