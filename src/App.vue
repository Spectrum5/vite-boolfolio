<script>
import { store } from './store';
import AppHeader from './components/AppHeader.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  name: "App",
  data() {
    return {
    }
  },
  components: {
    AppHeader,
    AppFooter
  },
  methods: {
  }
};
</script>

<template>
  <div class="container">
    <AppHeader />
    <main>
        <router-view></router-view>
    </main>
    <AppFooter />
  </div>
</template>

<style lang="scss">
@import './styles/main';
</style>