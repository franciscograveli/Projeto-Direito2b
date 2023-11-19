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
*{
  margin: 0 !important;
  padding: 0 !important;
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

  /* background: rgb(91,206,250);
  background: -moz-linear-gradient(180deg, rgba(91,206,250,1) 0%, rgba(245,169,184,1) 25%, rgba(255,255,255,1) 50%, rgba(245,169,184,1) 75%, rgba(91,206,250,1) 100%);
  background: -webkit-linear-gradient(180deg, rgba(91,206,250,1) 0%, rgba(245,169,184,1) 25%, rgba(255,255,255,1) 50%, rgba(245,169,184,1) 75%, rgba(91,206,250,1) 100%);
  background: linear-gradient(180deg, rgba(91,206,250,1) 0%, rgba(245,169,184,1) 25%, rgba(255,255,255,1) 50%, rgba(245,169,184,1) 75%, rgba(91,206,250,1) 100%);
  filter: progid:DXImageTransform.Microsoft.gradient(startColorstr="#5bcefa",endColorstr="#5bcefa",GradientType=1); */
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
