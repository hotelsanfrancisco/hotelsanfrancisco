<template>
  <Layout>
    <Intro bg="home">
      <p>
        Los invito seleccionar a nuestro Hotel para sus vacaciones. Será un
        placer tenerlos como nuestros huéspedes. Personalmente junto con mi
        equipo de colaboradores nos dedicaremos a garantizar que su estadía sea
        confortable, relajada y placentera.
      </p>
      <p><a href="/nuestro-hotel#lee-mas">Leer más acerca del hotel</a></p>
    </Intro>
    <section>
      <div class="container">
        <div class="row">
          <div class="col">
            <div id="habitaciones" class="h2 center mb-3">Habitaciones</div>
          </div>
        </div>
        <div class="row row-cols-1 row-cols-sm-2 row-cols-lg-4 g-4">
          <Card title="Habitación Doble" price="1100" image="room-2.jpeg" />
          <Card title="Habitación Triple" price="1500" image="room-3.jpeg" />
          <Card title="Habitación Cuadruple" price="1800" image="room-2.jpeg" />
          <Card title="Habitación Quintuple" price="2000" image="room-5.jpeg" />
        </div>
      </div>
    </section>
    <section class="pt-3 pb-5">
      <div class="container">
        <div class="row">
          <div class="col">
            <div id="galeria" class="h2 center mb-3">Galería</div>
          </div>
          <div class="col">
            <VueSlickCarousel v-bind="settings" class="slick">
              <img alt="fotos hostal" src="@/assets/photos/exterior-3.jpeg" />
              <img alt="fotos hostal" src="@/assets/photos/exterior-4.jpeg" />
              <img alt="fotos hostal" src="@/assets/photos/exterior-5.jpeg" />
              <img alt="fotos hostal" src="@/assets/photos/piscina-1.jpeg" />
              <img alt="fotos hostal" src="@/assets/photos/piscina-2.jpeg" />
              <img alt="fotos hostal" src="@/assets/photos/exterior-6.jpeg" />
              <img alt="fotos hostal" src="@/assets/photos/intro.jpeg" />
              <img alt="fotos hostal" src="@/assets/photos/room-2.jpeg" />
              <img alt="fotos hostal" src="@/assets/photos/room-3.jpeg" />
              <img alt="fotos hostal" src="@/assets/photos/room-5.jpeg" />
            </VueSlickCarousel>
          </div>
        </div>
      </div>
    </section>
  </Layout>
</template>

<script>
import Intro from "@/layouts/Intro.vue";
import Card from "@/components/Card.vue";

import VueSlickCarousel from "vue-slick-carousel";
import "vue-slick-carousel/dist/vue-slick-carousel.css";
// optional style for arrows & dots
import "vue-slick-carousel/dist/vue-slick-carousel-theme.css";

export default {
  components: {
    Intro,
    Card,
    VueSlickCarousel,
  },
  data() {
    return {
      settings: {
        focusOnSelect: true,
        draggable: true,
        dots: true,
        infinite: false,
        speed: 500,
        slidesToShow: 3,
        slidesToScroll: 3,
        initialSlide: 0,
        responsive: [
          {
            breakpoint: 1024,
            settings: {
              slidesToShow: 3,
              slidesToScroll: 3,
              infinite: true,
              dots: true,
            },
          },
          {
            breakpoint: 600,
            settings: {
              slidesToShow: 1,
              slidesToScroll: 1,
              initialSlide: 1,
            },
          },
        ],
      },
    };
  },
  metaInfo: {
    title: "Inicio",
  },
};
</script>

<style lang="scss" >
.slick {
  img {
    border-radius: 8px;
    border: 3px solid transparent;
  }
  .slick-arrow {
    @media screen and (max-width: 600px) {
      display: none !important;
    }
  }
}
</style>