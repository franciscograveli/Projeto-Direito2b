<script>

export default {
    name: 'Violences',
    props: {
        img: String,
        imgSide: String,
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
    <div class="violences">
        <template v-if="imgSide == 'l'">
            <div class="img flex-1" v-if="img">
                <img :src="`/assets/${img}`" alt="">
            </div>
            <div class="text flex-1">
                <slot></slot>
                <button v-if="button" >{{ button }}</button>
            </div>
        </template>
         <template v-else>
            <div class="text flex-1">
                <slot></slot>
                <button v-if="button" >{{ button }}</button>
            </div>
            <div class="img flex-1" v-if="img">
                <img :src="`/assets/${img}`" alt="">
            </div>
        </template>
    </div>
    
</template>

<style scoped>
.violences {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 100%;
    flex: 1 1 49% !important;
    margin: 1.5rem 0rem !important;
    position: relative;
    z-index: 0 !important;
    color: var(--white);
    transition: .5s ease all;
}

.text {
   
    flex: 2 1 50%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 1rem .5rem !important;
    font-size: 1.5rem;
    font-weight: bold;
    border-radius: .5rem;
    transition: .5s ease all;
    }
.text::before {
  content: "";
  position: absolute;
  inset: -5px; /* control the spread */
  transform: translate(10px, 8px); /* control the offsets */
  z-index: -1; /* place the element behind */
  background: linear-gradient(140deg, rgba(91,206,250,1) 0%, rgba(245,169,184,1) 100%);
  filter: blur(10px); /* control the blur */
}
.violences:hover{
    transition: .5s ease all;
    background-color: #f0f0f0;
    scale: 1.01;
}

.img{
    flex: 3 2 40%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    font-size: 1.5rem;
    width: 100%;
    height: 100%;
}
img{
    padding: 1rem !important;
    width: 100%;
    height: 100%;
}
</style>
