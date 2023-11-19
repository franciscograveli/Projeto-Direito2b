<script>

export default {
    name: 'TextModel',
    props: {
        color: String,
        button: Array,
        buttonColor: String
    },
    data() {
        return {
            backgroudColor: this.color? this.color : 'transparent'
        }
    }
}
</script>

<template>
    
    <div class="text" v-if="backgroudColor == 'blue'" 
    style="
     background: rgb(91,206,250);
    background: -moz-linear-gradient(344deg, rgba(91,206,250,1) 0%, rgba(245,169,184,1) 100%);
    background: -webkit-linear-gradient(344deg, rgba(91,206,250,1) 0%, rgba(245,169,184,1) 100%);
    background: linear-gradient(344deg, rgba(91,206,250,1) 0%, rgba(245,169,184,1) 100%);
    ">
        <slot></slot>
        <button v-if="button" >{{ button }}</button>
    </div>
    <div v-if="backgroudColor == 'blue-r'"  class="text"
        style="
        background: rgb(91,206,250);
    background: -moz-linear-gradient(140deg, rgba(91,206,250,1) 0%, rgba(245,169,184,1) 100%);
    background: -webkit-linear-gradient(140deg, rgba(91,206,250,1) 0%, rgba(245,169,184,1) 100%);
    background: linear-gradient(140deg, rgba(91,206,250,1) 0%, rgba(245,169,184,1) 100%);
    ">
        <slot></slot>
        <button v-if="button" >{{ button }}</button>
    </div>
    <div v-if="backgroudColor == 't'"  class="text"
        style="
        background-color: red;
        ">
        <slot></slot>
        <button v-if="button" >{{ button }}</button>
    </div>
</template>

<style scoped>
.text {
    max-width: 95vw;
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    margin: 2rem !important;
    padding: 1rem 2rem !important;
    font-size: 1.5rem;
    font-weight: bold;
    border-radius: .5rem;
    transition: .5s ease all;
    background: rgb(91,206,250);
    background: -moz-linear-gradient(344deg, rgba(91,206,250,1) 0%, rgba(245,169,184,1) 100%);
    background: -webkit-linear-gradient(344deg, rgba(91,206,250,1) 0%, rgba(245,169,184,1) 100%);
    background: linear-gradient(344deg, rgba(91,206,250,1) 0%, rgba(245,169,184,1) 100%);
    filter: progid:DXImageTransform.Microsoft.gradient(startColorstr="#5bcefa",endColorstr="#f5a9b8",GradientType=1);
    }
.text:hover{
    transition: .3s ease all;
    box-shadow: 0px 0px 15px 0px rgba(0, 0, 0, 0.13);
}
button{
    border-style: none;
    padding: 1rem 2rem !important;
    width: 50%;
    font-size: 1rem;
    font-weight: bold;
    margin: 1rem !important;
    border-radius: 2rem;
    cursor: pointer;
    color: white;
    transition: 0.5s ease all;
}

button:hover{
    transform: scale(1.01);
    transform: translate(px, -3px);
    transition: 0.5s ease all;
    box-shadow: 0px 0 10px 0px  rgba(0, 0, 0, 0.418);
}
button:active {
    transform: scale(0.99);
    transition: 0.5s ease all;
    box-shadow: 0px 0 10px 0px  rgba(0, 0, 0, 0.418);
    transform: translate(1px, 3px);

}
@media (min-width: 768px) {
    button{
        font-size: calc(0.75rem + 0.75vw);
    }
}

@media (min-width: 1024px) {
    button{
        font-size: 1rem;
    }
    
}
</style>
