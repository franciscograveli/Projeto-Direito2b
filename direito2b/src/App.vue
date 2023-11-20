<script setup>
import { RouterLink, RouterView } from 'vue-router';
import Nav from '@/components/Nav.vue';
import Footer from '@/components/Footer.vue';
</script>

<template>
    <div class="wrapper">
      <Nav />
      <RouterView />
      <Footer />
    </div>

  
</template>

<style>
:root{
  
  --color-background: #f0f0f0 !important;
  --color-primary-lighter: #9871f5;
  --color-primary-light: #916bea;
  --color-primary: #8257e5;
  --color-bright: #a78bfa;
  --blue: #5BCEFA;
  --pink: #F5A9B8;
  --white: white;
}
@font-face {
  font-family: 'inter-bold';
  src: url('./assets/fonts/static/Inter-Bold.ttf');
}
@font-face {
  font-family: 'inter';
  src: url('./assets/fonts/static/Inter-regular.ttf');
}
*{
  margin: 0 !important;
  padding: 0 !important;
  font-family: 'inter' ,Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
  
}
body{
  overflow-x: hidden;
}
h1{
  font-family: 'inter-bold' !important;
}
p, h1{
  text-align: center !important;
}
#app{
  margin: 0 !important;
  padding: 0 !important;
  width: 100%;
  height: 100%;
  min-width: 100vw;
  min-height: 100vh;
  display: flex !important;
  flex-direction: column !important;
  align-items: center;
  justify-content: center;
  background-color: #f0f0f0;
  
}
.wrapper{
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
}
header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    /* padding-right: calc(var(--section-gap) / 2); */
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
    /* animation */
@keyframes trans-color {
    0% {
        text-decoration-color: var(--blue);
    }
    50% {
        text-decoration-color: var(--pink);
    }
    100% {
        text-decoration-color: var(--blue);
    }
}
}
</style>
