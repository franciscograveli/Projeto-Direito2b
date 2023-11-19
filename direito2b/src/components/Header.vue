<script>
export default {
    name: 'Header',
    props: {
        text: String
    },

}
</script>

<template>
<header>
    <div class="main-banner">
        <p>{{ text }}</p>
    </div>
</header>
</template>

<style scoped>
.main-banner {
    background-image: url('src/assets/img/mainbanner-img.jpg');
    background-size: contain; /* Garante que a imagem inteira seja visível */
    background-repeat: no-repeat; /* Evita que a imagem se repita */
    background-position: center; /* Centraliza a imagem no banner */

    width: 100vw !important;
    min-height: 300px;
    height: 50vh;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    gap: 10px;
    text-align: center;
    color: white;
}
header {
  margin: 0;
  padding: 0;
  overflow-x: hidden;
  background-color: black;
}
p{
  width: 60%;
  min-width: 300px;
  font-size: 1.5rem;
  font-weight: bold;
  text-align: center;
}
p::before{
  position: absolute;
  content: "";
  display: flex;
  width: 10px;
  height: 13vh;
  border-radius: 2rem;
  transform: translateX(-10px);
  background-color: var(--color-bright);

}

@media (max-width: 768px) {
    p::before{
        display: none;
    }
    p{
        background-color: var(--color-bright);
        opacity: 0.8;
        padding: 1rem !important;
        border-radius: 1rem;
        border: 2px solid var(--color-bright);
    }
}
</style>