<template>
  <div class="flex flex-col min-h-screen font-Roboto bg-weather-primary">
    <SiteNavigation />
    <RouterView v-slot="{ Component }">
      <Transition name="page" mode="out-in">
        <component :is="Component"></component>
      </Transition>
    </RouterView>
  </div>
</template>
<div>
<h1>
  Hallo
</h1>
</div>

<script>
import { RouterView } from "vue-router";
import SiteNavigation from "./components/SiteNavigation.vue";

export default {
  components: {
    RouterView,
    SiteNavigation,
  },
};
</script>

<style>
.page-enter-active,
.page-leave-active {
  transition: 600ms ease all;
}

.page-enter-from,
.page-leave-to {
  opacity: 0;
  transform: translateX(100%);
}
</style>
