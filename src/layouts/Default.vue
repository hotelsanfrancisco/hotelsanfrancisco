<template>
  <div class="layout">
    <header class="container-fluid">
      <div class="row">
        <div class="col">
          <nav>
            <div>
              <a href="/">
                <g-image
                  alt="Inicio"
                  src="~/assets/logo-green.svg"
                  width="85"
                />
                <g-link class="site-name" to="/">{{
                  $static.metadata.siteName
                }}</g-link>
              </a>
            </div>
            <div class="nav-right">
              <router-link to="/#habitaciones">Habitaciones</router-link>
              <router-link to="/nuestro-hotel">Conozca el Hotel</router-link>
              <router-link to="/contacto">Contacto</router-link>
            </div>
          </nav>
        </div>
      </div>
    </header>
    <slot />
    <section>
      <div class="container">
        <div class="row">
          <div class="col-12 col-sm-6 mb-4 contacto">
            <div class="h1">Llámenos para reservar</div>
            <div class="h0 mb-3">414 27 302 31 <br /></div>

            <iframe
              src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3736.5586510631324!2d-99.89508348572961!3d20.524311186273785!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x85d39dfd7d0a92cf%3A0x4f4c837c0f0fcb33!2sPosada%20San%20Francisco!5e0!3m2!1sen!2ses!4v1635988316111!5m2!1sen!2ses"
              style="border: 0"
              allowfullscreen=""
              loading="lazy"
            ></iframe>
            <div class="h4 pt-2">
              Puedes encontrarnos en: Moctezuma 2, Centro, 76750 Tequisquiapan,
              Qro., Mexico
            </div>
          </div>
          <div class="col-12 col-sm-6">
            <div class="h2">Esto es Tequisquiapan</div>
            <div class="video-responsive">
              <iframe
                src="https://www.youtube.com/embed/hD56Mt0K3GA"
                title="YouTube video player"
                frameborder="0"
                allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
                allowfullscreen
              ></iframe>
            </div>
          </div>
        </div>
      </div>
    </section>
    <footer class="block pt-3">
      <div class="container">
        <div class="row">
          <div class="col footer-group">
            <div class="mb-2">
              <a href="/">
                <g-image
                  alt="Inicio"
                  src="~/assets/logo-white.svg"
                  width="80"
                />
              </a>
            </div>
            <div class="mb-2">
              <router-link to="/#habitaciones" class="pe-4"
                >Habitaciones</router-link
              >
              <router-link to="/nuestro-hotel" class="pe-4"
                >Conozca el Hotel</router-link
              >
              <router-link to="/contacto">Contacto</router-link>
            </div>
            <div class="mb-2">
              <a href="facebook">
                <svg
                  aria-hidden="true"
                  focusable="false"
                  role="img"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 512 512"
                  class="footer-svg"
                >
                  <path
                    fill="currentColor"
                    d="M504 256C504 119 393 8 256 8S8 119 8 256c0 123.78 90.69 226.38 209.25 245V327.69h-63V256h63v-54.64c0-62.15 37-96.48 93.67-96.48 27.14 0 55.52 4.84 55.52 4.84v61h-31.28c-30.8 0-40.41 19.12-40.41 38.73V256h68.78l-11 71.69h-57.78V501C413.31 482.38 504 379.78 504 256z"
                  ></path>
                </svg>
              </a>
            </div>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style lang="scss" scoped>
.layout {
  background-color: var(--color-bg);
  color: var(--color-text);
  font-size: 21px;
  line-height: 24px;
}

nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-top: 10px;
  font-weight: bold;
  a {
    margin-left: 15px;
    &:hover {
      color: var(--color-text);
    }
  }
}

iframe {
  max-width: 90%;
}

.nav-right {
  @media screen and (max-width: 550px) {
    display: flex;
    flex-direction: column;
  }
}

.contacto {
  justify-content: center;
  display: flex;
  flex-direction: column;
}

.video-responsive {
  height: 0;
  overflow: hidden;
  padding-bottom: 56.25%;
  padding-top: 30px;
  position: relative;
}
.video-responsive iframe,
.video-responsive object,
.video-responsive embed {
  height: 100%;
  left: 0;
  position: absolute;
  top: 0;
  width: 100%;
}

footer {
  @media screen and (max-width: 550px) {
    padding-bottom: 10px;
  }
}
  
.footer {
  &-group {
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;

    @media screen and (max-width: 550px) {
      flex-direction: column;
      text-align: center;
    }
  }
  &-svg {
    width: 24px;
  }
}

@media screen and (max-width: 740px) {
  .site-name {
    display: none;
  }
}
</style>
