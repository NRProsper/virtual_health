<script setup>
import Menu from "vue-material-design-icons/Menu.vue";
import Close from "vue-material-design-icons/Close.vue";

import {onMounted, ref, watch} from "vue";
import HomeView from "@/views/HomeView.vue";
import Services from "@/components/Services.vue";

const isOpen = ref(false);
const toggleMenu = () => {
  isOpen.value = !isOpen.value;
}

watch(isOpen, (newVal) => {
  if(newVal) {
    document.body.classList.add("no-scroll");
  }else {
    document.body.classList.remove("no-scroll");
  }
})


</script>

<template>
  <header class="flex">
    <div class="container">
      <div class="navigation flex justify-between">
        <a href="#" class="logo">
          <img src="./assets/img/logo.svg" alt="Logo Image">
        </a>
        <nav :class="['nav-links', {open : isOpen}]">
          <a href="#" class="active">Home</a>
          <a href="#">Find doctor</a>
          <a href="#">Apps</a>
          <a href="#">Testimonials</a>
          <a href="#">Contact us</a>
        </nav>
        <div class="menu-toggle" @click="toggleMenu">
          <Menu v-if="!isOpen" />
          <Close v-else />
        </div>
      </div>
    </div>
  </header>

  <main>
    <HomeView />
    <Services />
  </main>
</template>

<style scoped>
@media only screen and (max-width: 768px) {
  .nav-links {
    z-index: 9999;
    //display: none;
    position: absolute;
    top: 80px;
    left: 0;
    right: 0;
    height: calc(100vh -  80px);
    visibility: hidden;
    background: var(--vh-body-background);
    //width: 100vw;
    //transition: all 0.3s ease-in-out;

    display: flex;
    align-items: center;
    justify-content: center;
    flex-flow: column;
    gap: 20px;
  }

  .nav-links a {
    margin-right: 0;
    border-bottom: 1px solid var(--vh-nav-text);
    width: 200px;
    text-align: center;
  }

  .nav-links.open {
    visibility: visible;
  }


  .menu-toggle {
    display: inline-flex;
  }
}
</style>
