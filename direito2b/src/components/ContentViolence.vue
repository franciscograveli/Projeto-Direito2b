<script>
import TextModel from '@/components/TextModel.vue';
import Violences from '@/components/Violences.vue';
import Scoopes from '@/components/Scoopes.vue';
export default {
    name: 'ContentViolence',
    components: {
        Violences,
        Scoopes
    }

}
</script>

<template>
    <div class="content">
       <Violences color="blue-r" img="src/assets/img/bannerLei.png" imgSide="l">
            <div class="textSlot">
                <h1>Violência Sexual:</h1>
                <p>
                     A violência sexual envolve qualquer ato sexual não consensual ou coercitivo realizado contra a vontade da vítima. Isso inclui estupro, agressões sexuais, coerção para atividades sexuais indesejadas, pornografia não consensual e outras formas de exploração sexual. A violência sexual é uma grave violação dos direitos da vítima e pode causar traumas profundos.
                </p>
            </div>
        </Violences>
         <Violences color="blue-r" img="src/assets/img/bannerLei.png">
            <div class="textSlot">
                <h1>Violência Sexual:</h1>
                <p>
                     A violência sexual envolve qualquer ato sexual não consensual ou coercitivo realizado contra a vontade da vítima. Isso inclui estupro, agressões sexuais, coerção para atividades sexuais indesejadas, pornografia não consensual e outras formas de exploração sexual. A violência sexual é uma grave violação dos direitos da vítima e pode causar traumas profundos.
                </p>
            </div>
        </Violences>
        <Violences color="blue-r" img="src/assets/img/bannerLei.png" imgSide="l">
            <div class="textSlot">
                <h1>Violência Sexual:</h1>
                <p>
                     A violência sexual envolve qualquer ato sexual não consensual ou coercitivo realizado contra a vontade da vítima. Isso inclui estupro, agressões sexuais, coerção para atividades sexuais indesejadas, pornografia não consensual e outras formas de exploração sexual. A violência sexual é uma grave violação dos direitos da vítima e pode causar traumas profundos.
                </p>
            </div>
        </Violences>
        <Scoopes />
    </div>
</template>

<style scoped>

.content{
    display: flex !important;
    flex-direction: column !important;
    flex-wrap: wrap !important;
    justify-content: center !important;
    align-items: start !important;
    margin: 1rem !important;
    padding: 20px;
    gap: 1rem;
    color: black;
    max-width: 99vw;
}
.side{
    flex: 1 1 50%;
    gap: 1rem;
    display: flex !important;
    flex-direction: column !important;
    justify-content: center !important;
    align-items: center !important;
}
.textSlot{
    padding: 1rem 2rem !important;
    display: flex !important;
    flex-direction: column !important;
    justify-content: center !important;
    align-items: center !important;
}

h1{
    font-size: 2rem;
}
p{
    font-size: 1.5rem;
    line-height: 1.5;
    text-align: justify;
}
img{
    max-width: 500px;
    width: 100%;
    height: 100%;
    object-fit: cover;
    
}
</style>