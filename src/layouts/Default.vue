<template>
  <div class="layout">
    <header class="container-fluid">
      <div class="row">
        <div class="col">
          <nav>
            <!-- <g-link to="/">{{ $static.metadata.siteName }}</g-link> -->
            <div class="nav-left">
              <a href="/">
                <g-image alt="Example image" src="~/favicon.png" width="50" />
              </a>
            </div>
            <div class="nav-right">
              <router-link to="/config-user">Habitaciones</router-link>
              <router-link to="/config-mail">Nuestra Historia</router-link>
              <router-link to="/config-mail">Contacto</router-link>
            </div>
          </nav>
        </div>
      </div>
    </header>
    <slot />
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style>
:root {
  --color-bg: #f8efea;
  --color-text: #333;
  --color-block: #7b9e89;
  --color-btn: rgba(199, 112, 44);
}

.layout {
  background-color: var(--color-bg);
  color: var(--color-text);
  font-size: 18px;
  line-height: 24px;
}

nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 0;
  font-weight: bold;
}

nav a {
  margin-left: 15px;
}

nav a:hover {
  color: var(--color-text);
}

.nav__link {
  margin-left: 20px;
}
</style>
