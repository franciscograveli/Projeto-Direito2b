<script>
export default {
    name: 'Nav',
    methods: {
        scrool(){
            window.scrollTo(0, 0);
            document.addEventListener("scroll", function(){
                const nav = document.querySelector("nav");
                if(window.scrollY > 100){
                    nav.classList.add("scrolled");
                }else{
                    if(nav.classList.contains("scrolled")){
                        nav.classList.remove("scrolled");
                    }
                }
            });
        }
    },
    mounted(){
        this.scrool();
    }
}
</script>

<template>
    <nav>
        <ul>
            <li>
                <router-link to="/">
                    <p>Home</p>
                </router-link>
            </li>
            <li>
                <router-link to="/violence">
                    <p>A Violência</p>
                </router-link>
            </li>
        </ul>
    </nav>

</template>

<style scoped>
nav {
    z-index: 2;
    transition: .5s ease all;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    min-height: 50px;
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 1rem;
    background-color: transparent;
}
ul{
    padding: 1rem 2rem;
    display: flex;
    gap: 1rem;
    justify-content: center;
    align-items: center;
    list-style: none;
}
ul a{
    color: white;
}
a:hover{
    text-decoration: underline;
    text-underline-position: 1rem;
    animation: trans-color 3s infinite;
    cursor: pointer;
    background-color: transparent;
}
.scrolled{
    transition: .5s ease all;
    background: rgb(153,153,153);
    background: linear-gradient(0deg, rgba(153, 153, 153, 0) 0%, rgba(0, 0, 0, 0.63) 100%);
   } 

</style>