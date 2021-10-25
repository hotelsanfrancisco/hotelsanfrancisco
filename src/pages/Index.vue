<template>
  <Layout>
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
        <div class="col intro-right"></div>
      </div>
    </div>
    <div class="container-fluid block">
      <div class="row">
        <div class="col-md-9 block-info">
          <p>
            Los invito seleccionar a nuestro Hotel para sus vacaciones. Será un
            placer tenerlos como nuestros huéspedes.
          <br/>
            Personalmente junto con mi equipo de colaboradores nos dedicaremos a
            garantizar que su estadía sea confortable, relajada y placentera.
          </p>
          <p><a href="/nuestro-hotel">Leer más acerca del hotel</a></p>
        </div>
      </div>
    </div>
    <section>
      <div class="container">
        <div class="row">
          <div class="col">
            <div class="h3 center">Habitaciones</div>
          </div>
        </div>
      </div>
    </section>
  </Layout>
</template>

<script>
    export default {
      metaInfo: {
        title: 'Hello, world!'
      }
    }
    </script>

<style>

.h1 {
  font-size: 32px;
  line-height: 38px;
  font-weight: 900;
}

.h2 {
  font-size: 24px;
  line-height: 28px;
  font-weight: 900;
}

.h3 {
  font-size: 24px;
  line-height: 28px;
  font-weight: 400;
}

a {
  color: var(--color-text);
  text-decoration: none;
}



.btn-primary {
  background-color: var(--color-btn) !important;
  border-color: var(--color-btn) !important;
}

.intro-left {
  padding: 0 4%;
  margin: 20px 0;
  flex-direction: column;
  justify-content: center;
}

.intro-right {
  background: url('../assets/photos/intro.jpeg') no-repeat;
  background-size: cover;
  min-height: 500px;
  background-position: 50% 50%;
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
  .intro-left {
    padding: 0;
  }
  .intro-right {
    min-height: 250px;
  }
}

section {
  padding: 20px 0;
}

.center {
  text-align: center;
}

.block {
  background-color: var(--color-block);
  color: white;
}

.block a {
  color: var(--color-text);
}

.block-info {
  padding: 30px 0 10px;
  text-align: center;
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  margin: 0 auto;
}
</style>
