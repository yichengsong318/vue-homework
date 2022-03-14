<template>
  <q-layout view="lHh Lpr lFf">
    <q-page-container>
      <div class="background" />
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "MainLayout",
});
</script>

<style lang="scss">
.background {
  background: #11082f;
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}

@media (max-width: $breakpoint-xs-max) {
  .background {
    background: #442c5c;
    width: 100%;
    height: 100%;
  }
}
</style>
