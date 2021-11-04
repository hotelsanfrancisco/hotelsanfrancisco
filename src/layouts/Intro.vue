<template>
  <div>
    <div class="container-fluid">
      <div class="row flex-row">
        <div class="col-md-6 d-flex intro-left">
          <div class="h1">
            Disfruta de tu estancia en el hotel posada San Francisco
          </div>
          <p>Pregunta precios y disponibilidad</p>
          <div>
            <a href="/contacto" class="btn btn-primary"> Contacto </a>
          </div>
        </div>
        <div class="col intro-right" :class="`intro-right-${bg}`"></div>
      </div>
    </div>
    <div class="block">
      <div class="container">
        <div class="row">
          <div class="col-12 block-info">
            <slot></slot>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["bg"],
};
</script>

<style lang="scss" scoped>
.intro-left {
  padding: 0 4%;
  margin: 20px 0;
  flex-direction: column;
  justify-content: center;
}

.intro-right {
  background-repeat: no-repeat;
  background-size: cover;
  min-height: 500px;
  background-position: 50% 50%;
  background-image: var(--background-url);
  &-home {
    background-image: url("../assets/photos/intro.jpeg");
  }
  &-hotel {
    background-image: url("../assets/photos/exterior-6.jpeg");
  }
}

@media screen and (max-width: 768px) {
  .intro-left {
    padding: 0 4%;
  }
  .intro-right {
    min-height: 250px;
  }
}

@media screen and (max-width: 480px) {
  .intro-right {
    min-height: 250px;
  }
}
</style>
