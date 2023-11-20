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
       <Violences color="blue-r" img="fisica.svg" imgSide="l">
            <div class="textSlot">
                <h1>Violência Física:</h1>
                <p>
                    A violência física envolve a aplicação de força física com a intenção de causar dano ao corpo da vítima. Isso pode incluir socos, chutes, empurrões, estrangulamento, tapas, mordidas, queimaduras, entre outros atos agressivos. As lesões resultantes da violência física variam em gravidade, desde hematomas leves até ferimentos graves ou até mesmo a morte.
                </p>
            </div>
        </Violences>
         <Violences color="blue-r" img="moral.svg">
            <div class="textSlot">
                <h1>Violência Moral:</h1>
                <p>
                    A violência moral, também conhecida como violência verbal ou psicológica, consiste em comportamentos que têm o objetivo de desvalorizar, humilhar, menosprezar ou envergonhar a vítima. Isso pode incluir xingamentos, insultos, degradação verbal, ridicularização, ameaças, difamação, chantagem emocional, isolamento social e qualquer forma de manipulação psicológica que cause sofrimento à vítima. 
                </p>
            </div>
        </Violences>
        <Violences color="blue-r" img="sexual.svg" imgSide="l">
            <div class="textSlot">
                <h1>Violência Sexual:</h1>
                <p>
                    A violência sexual envolve qualquer ato sexual não consensual ou coercitivo realizado contra a vontade da vítima. Isso inclui estupro, agressões sexuais, coerção para atividades sexuais indesejadas, pornografia não consensual e outras formas de exploração sexual. A violência sexual é uma grave violação dos direitos da vítima e pode causar traumas profundos.
                </p>
            </div>
        </Violences>
        <Violences color="blue-r" img="patrimonial.svg" >
            <div class="textSlot">
                <h1>Violência Patrimonial:</h1>
                <p>
                    A violência patrimonial se refere ao controle ou destruição dos bens e recursos da vítima, com o objetivo de torná-la economicamente dependente ou prejudicá-la financeiramente. Isso pode incluir o roubo de dinheiro, a destruição de propriedades, a recusa em fornecer recursos financeiros para as despesas da vítima e outras ações que afetam negativamente seu patrimônio.
                </p>
            </div>
        </Violences>
        <Violences color="blue-r" img="psicologica.svg" imgSide="l">
            <div class="textSlot">
                <h1>Violência Psicológica:</h1>
                <p>
                    A violência psicológica envolve a manipulação sistemática da mente da vítima, com o objetivo de controlar seu comportamento, emoções e pensamentos. Isso pode incluir o isolamento da vítima de amigos e familiares, vigilância constante, controle excessivo, chantagem emocional, ameaças de morte ou de prejudicar a si mesma, entre outras táticas de controle mental.
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
    gap: 1rem;
    color: black;
    max-width: 90vw;
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