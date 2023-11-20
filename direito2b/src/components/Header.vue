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
    background-image: url('/src/assets/img/banner.svg');
    background-size: contain; 
    background-repeat: no-repeat; 
    background-position: center; 

    width: 100vw !important;
    min-width: 320px;
    min-height: 400px;
    height: auto;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    gap: 10px;
    text-align: center;
    color: var(--white);
    position: relative;
    z-index: 1;
}
.main-banner::before{
        width: 100%;
        height: 150%;
        content: "";
        position: absolute;
        inset: -5px; /* control the spread */
        transform: translate(10px, -25%); /* control the offsets */
        z-index: -1; /* place the element behind */
        opacity: 1;
        background: rgba(0, 0, 0, 0.37);
        filter: blur(20px); /* control the blur */
    }
header {
  margin: 0;
  padding: 0;
  overflow-y: hidden;
  overflow-x: hidden;
  background-color: var(--white);
  
}
p{
  width: 60%;
  min-width: 300px;
  font-size: 1.5rem;
  font-weight: bold;
  text-align: center;
  position: relative;
  z-index: 1;
}
p::before{
  position: absolute;
  content: "";
  display: flex;
  width: 10px;
  height: 13vh;
  border-radius: 2rem;
  transform: translateX(-10px);
  background: linear-gradient(
  140deg,
  var(--blue) 10%,    
  var(--pink) 30%,   
  var(--white) 50%,
  var(--pink) 70%,   
  var(--blue) 90%  
);
}



@media (max-width: 768px) {
    
    p::before{
        display: none;
    }
    p{
        background-color: transparent;
        opacity: 1;
        padding: 1rem !important;
        border-radius: 1rem;
        border: none;
    }
}
</style>