<script>
import TextModel from '@/components/TextModel.vue';
export default {
    name: 'ContentHome',
    components: {
        TextModel
    }

}
</script>

<template>
    <div class="content">
       <div class="side">
          <TextModel color="blue" >
            <div class="textSlot">
                <h1>Existe diferença de violência contra a mulher cis e a mulher trans?  </h1>
                <p>
                    •A violência doméstica contra mulheres cis e mulheres trans é um problema grave que envolve a agressão física, psicológica, sexual, econômica e/ou verbal direcionada a uma mulher por parte de um parceiro íntimo ou membro da família em um ambiente doméstico. A principal diferença é que mulheres trans enfrentam desafios específicos devido à discriminação de gênero e transfobia, o que torna a violência que sofrem ainda mais complexa. Muitas vezes, mulheres trans enfrentam discriminação dupla, tanto como mulheres quanto como pessoas trans, tornando-as particularmente vulneráveis a abusos.
                </p>
            </div>
        </TextModel>
        <TextModel color="blue-r">
            <div class="textSlot">
            <h1>Reconhecer uma violência doméstica é muito importante!  </h1>
            <p>
                •É importante reconhecer que todas as formas de violência doméstica são inaceitáveis e ilegais, e é fundamental combater essa violência, fornecer apoio às vítimas e promover a conscientização sobre os desafios específicos enfrentados por mulheres cis e trans. Além disso, leis e políticas têm sido implementadas em muitos lugares para proteger as vítimas e punir os agressores, independentemente de sua identidade de gênero.
            </p>
            </div>
        </TextModel >
       </div>
       <div class="side">
            <img src="src/assets/img/bannerLei.png" alt="Banner Sobre a lei maria da penha">
       </div>
    </div>
</template>

<style scoped>

.content{
    display: flex !important;
    flex-direction: row !important;
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