<template>
  <footer>
    <div class="section no-gap">
        <lord-icon
            src="https://cdn.lordicon.com/rsvfayfn.json"
            trigger="hover"
            colors="primary:#e83a30"
            style="
            width:32px;
            height:32px;">
        </lord-icon>    
        <h2>181</h2>
    </div>
    <div class="section">
    <img src="src/assets/img/logo_faminas.png" alt="">
    <ul @click="active" :class="{ 'active': isActive, 'img': !isActive }" id="ulFooter">
      <template v-if="isActive">
        <li v-for="account in instagramAccounts" :key="account" @click="abrirInstagram(account)">@{{ account }}</li>
        <p @click="active">Fechar</p>
      </template>
    </ul>
    </div>
    <div class="section">
        <p>Direitos reservados Direito2b © 2023</p>
    </div>
    
  </footer>
</template>

<script>
export default {
  name: 'Footer',
  watch: {
    isActive(newValue) {
      var ul = document.getElementById("ulFooter");
      if (newValue) {
        ul.classList.add("active");
      } else {
        ul.classList.remove("active");
      }
    }
  },
  data() {
    return {
      isActive: false,
      instagramAccounts: [
        'dirceuarchete',
        'emanuel.alef_',
        'paolla__hellenaa',
        'yaasmin_januario',
        'greicesilva_1',
        'beatrizzvieira1108',
        'andre.lmotta',
        'florrane'
      ]
    };
  },
  methods: {
    active() {
      if (!this.isActive) {
        this.isActive = true;
      }else{
        this.isActive = false;
      }
    },
    abrirInstagram(account) {
        window.open(`https://www.instagram.com/${account}/`, "_blank");
      console.log("abrirInstagram");
    },
    ascInstagram() {
    this.instagramAccounts.sort();
  },
  },
  mounted() {
    this.ascInstagram();
    
  }
};
</script>

<style lang="scss" scoped>
* {
  transition: 0.5s ease all;
  color: var(--color-background);
}

footer {
  position: relative;
  min-height: 200px;
  height: 100%;
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 1rem;
  background-color: var(--color-background);
  box-shadow: inset 0 0 100px 100px #999999;
}


img {
  width: 100%;
  max-width: 48px;
}

ul {
  width: 100%;
  max-width: 48px;
  height: 48px;
  background-color: transparent;
  padding: 1rem 2rem;
  display: flex;
  flex-direction: column;
  gap: 1rem;
  justify-content: center;
  align-items: center;
  list-style: none;
  cursor: pointer;
}


img:hover {
  transition: 0.5s ease all;
  cursor: pointer;
  transform: translate(0, -5px);
  scale: 1.01;
}

li:hover{
  transition: 0.5s ease all;
  animation: trans-color 3s infinite;
}
p {
    color: #ddd;
}
p:hover{
    color: red;
}

h2{
    font-weight: bolder;
    color: white;
}

ul a {
  color: white;
}

a:hover {
  text-decoration: underline;
  text-underline-position: 1rem;
  animation: trans-color 3s infinite;
  cursor: pointer;
  background-color: transparent;
}
.active {
  position: absolute;
  background-color: var(--white);
  transform: translate(0, -10rem);
  height: 100%;
  min-height: 100px;
  width: 100%;
  max-width: 200px;
  overflow-y: auto;
  border-radius: 1rem;
  box-shadow: 0 0 10px 0px rgba(0, 0, 0, 0.199);
}
.img {
  background-image: url('src/assets/img/instagram.png');
  background-size: contain;
  background-repeat: no-repeat;
  background-position: center;
}
.section {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  gap: 1rem;
  width: 100%;
}
.no-gap{
    gap: 0;
}
/* animation */
@keyframes trans-color {
  0% {
    color: var(--blue);
    text-decoration-color: var(--blue);
  }
  50% {
    color: var(--pink);
    text-decoration-color: var(--pink);
  }
  100% {
    color: var(--blue);
    text-decoration-color: var(--blue);
  }
}
</style>
