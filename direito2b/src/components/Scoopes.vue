<template>

  <div class="carrousel d-flex-center">
    <swiper  class="mySwiper">
      <swiper-slide>
            <h1>Âmbito Doméstico:</h1>
            <p>
                O âmbito doméstico refere-se ao ambiente da casa ou residência onde as pessoas convivem. A violência doméstica que ocorre nesse contexto envolve agressões e maus-tratos que têm lugar dentro do ambiente doméstico, independentemente dos laços de parentesco ou afetivos entre as pessoas envolvidas. Isso pode incluir, por exemplo, violência entre cônjuges, parceiros de vida ou companheiros de moradia.
            </p>
      </swiper-slide>
      <swiper-slide>
            <h1>Âmbito Doméstico:</h1>
            <p>
                O âmbito doméstico refere-se ao ambiente da casa ou residência onde as pessoas convivem. A violência doméstica que ocorre nesse contexto envolve agressões e maus-tratos que têm lugar dentro do ambiente doméstico, independentemente dos laços de parentesco ou afetivos entre as pessoas envolvidas. Isso pode incluir, por exemplo, violência entre cônjuges, parceiros de vida ou companheiros de moradia.
            </p>
      </swiper-slide>
      <swiper-slide>
            <h1>Âmbito Doméstico:</h1>
            <p>
                O âmbito doméstico refere-se ao ambiente da casa ou residência onde as pessoas convivem. A violência doméstica que ocorre nesse contexto envolve agressões e maus-tratos que têm lugar dentro do ambiente doméstico, independentemente dos laços de parentesco ou afetivos entre as pessoas envolvidas. Isso pode incluir, por exemplo, violência entre cônjuges, parceiros de vida ou companheiros de moradia.
            </p>
      </swiper-slide>
      <swiper-slide>
            <h1>Âmbito Doméstico:</h1>
            <p>
                O âmbito doméstico refere-se ao ambiente da casa ou residência onde as pessoas convivem. A violência doméstica que ocorre nesse contexto envolve agressões e maus-tratos que têm lugar dentro do ambiente doméstico, independentemente dos laços de parentesco ou afetivos entre as pessoas envolvidas. Isso pode incluir, por exemplo, violência entre cônjuges, parceiros de vida ou companheiros de moradia.
            </p>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/pagination';
import { Pagination } from 'swiper/modules';

export default {
  name: 'Scoopes',
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      pagination: {
        clickable: true,
        renderBullet: function (index, className) {
          return '<span class="' + className + '">' + (index + 1) + '</span>';
        },
      },
      modules: [Pagination],
    };
  },
};
</script>

<style scoped>
span{
  margin-top: 1rem !important;
  font-size: .9rem;
  text-align: center;
  color: rgb(0, 0, 0);
  padding: .5rem;
}
.d-flex-center{
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
.carrousel {
  z-index: 1;
  width: 100%;
  height: 100%;
  min-height: 50vh;
  padding: 1rem 2rem !important;
}

.swiper {
  width: 100%;
  height: 100%;
}

.swiper-slide {
  text-align: center;
  font-size: 18px;
  width: 100%;
  height: 100%;

  /* Center slide text vertically */
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.swiper-slide video {
  max-width: 1000px;
  width: 100%;
  border-radius: .5rem;
  box-shadow: 0 0 10px 0px rgba(0, 0, 0, 0.356);
}

.swiper-pagination-bullet {
  width: 100px;
  height: 20px;
  text-align: center;
  line-height: 20px;
  font-size: 12px;
  animation: trans-color 3s infinite !important;
  opacity: 1;
  background: rgba(0, 0, 0, 0.2);
}

.swiper-pagination-bullet-active {
  color: #fff;
  background: #007aff;
}
.swiper-pagination-bullet span{
    animation: trans-color 3s infinite !important;
}
</style>