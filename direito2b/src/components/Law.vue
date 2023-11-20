<script>
export default {
    name: 'Law',
}
</script>

<template>
    <div class="law">
        <div class="text">
        <h1>A Lei Maria da Penha</h1>
        <p>
           De acordo com o art. 5º da Lei Maria da Penha, violência doméstica e familiar contra a mulher é “qualquer ação ou omissão baseada no gênero que lhe cause morte, lesão, sofrimento físico, sexual ou psicológico e dano moral ou patrimonial”.
        </p>
        </div>
    </div>
</template>

<style scoped>

.law{
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 0rem;
    padding: 20px !important;
    color: black;
}
.text{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 1rem;
    padding: 1rem 2rem !important;
    width: 80%;
    min-width: 300px;
    max-width: 1200px;
}

h1{
    font-size: 2rem;
}
p{
    font-size: 1.5rem;
}
</style>