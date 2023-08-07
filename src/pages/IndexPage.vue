<template>
  <q-page>
    <!-- Header -->
    <header>
      <div class="row justify-center">
        <!-- Logo -->
        <div class="col-12 col-md-6">
          <img src="~assets/logo.png" alt="" />
        </div>
        <!-- Botones -->
        <div class="col-12 col-md-6">
          <div
            class="col-xs-2 col-sm-2 col-md-8 menu-nav justify-end"
          >
            <q-btn class="open-menu q-mt-sm" @click="toggleNav" icon="ti-menu" flat />
            <nav class="nav" ref="nav" id="nav">
              <q-list class="nav-list">
                <q-item
                  clickable
                  v-ripple
                >
                  <q-item-section>
                    <q-btn
                      class="closed-menu"
                      @click="toggleNavs"
                      icon="ti-close"
                      flat
                    />
                  </q-item-section>
                </q-item>
                <q-item
                  clickable
                  v-ripple
                  class="list_item"
                  @click="IndexPage"
                  to="/"
                  active-class="my-menu-link"
                  exact
                >
                  <q-item-section>Inicio</q-item-section>
                </q-item>
                <q-item
                  clickable
                  v-ripple
                  class="list_item"
                  active-class="my-menu-link"
                >
                  <q-item-section>Sobre Nosotros</q-item-section>
                </q-item>
                <q-item
                  clickable
                  v-ripple
                  class="list_item"
                  active-class="my-menu-link"
                >
                  <q-item-section>Adoptar</q-item-section>
                </q-item>
                <q-item
                  clickable
                  v-ripple
                  class="list_item"
                  active-class="my-menu-link"
                >
                  <q-item-section>Contactenos</q-item-section>
                </q-item>
              </q-list>
            </nav>
          </div>
        </div>
      </div>
    </header>
    <!-- Banner -->
    <div class="zona1 row flex flex-center">
      <!-- Texto del Banner -->
      <div class="col-10">
        <h3 style="color: #26a69a">Encuentre su Mascota</h3>
        <p style="color: #000">
          Cuando ayudas o adoptas un animal estas opteniendo un pedazo de
          historia
        </p>
      </div>
    </div>
    <!-- Button con Phone Number -->
    <div class="row justify-center">
      <div class="col-10" id="phonebtn">
        <q-btn label="+53 52519414" rounded class="bg-white" />
      </div>
    </div>
    <!-- Componentes -->
    <Seccion1Dialog />
    <EssentialLinkcopy2 />
    <EssentialLinkcopy3 />
    <EssentialLinkcopy5 />
    <EssentialLinkcopy4 />
    <EssentialLinkcopy7 />
  </q-page>
</template>

<script setup>
// Importacion de los Componentes
import Seccion1Dialog from "src/components/Seccion1Dialog.vue";
import EssentialLinkcopy2 from "src/components/EssentialLinkcopy2.vue";
import EssentialLinkcopy3 from "src/components/EssentialLinkcopy3.vue";
import EssentialLinkcopy4 from "src/components/EssentialLinkcopy4.vue";
import EssentialLinkcopy5 from "src/components/EssentialLinkcopy5.vue";
import EssentialLinkcopy7 from "src/components/EssentialLinkcopy7.vue";

import { ref } from 'vue';

const nav = ref(null)
const toggleNav = () => {
  nav.value.classList.add('visibility')
};
const toggleNavs = () => {
  nav.value.classList.remove('visibility')
};

// Efecto Scroll Bar
window.addEventListener("scroll", function () {
  var header = document.querySelector("header");
  header.classList.toggle("abajo", window.scrollY > 0);
});
</script>

<!-- Estilos y efectos scss -->
<style>
header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  justify-content: space-around;
  transition: 0.7s;
  padding: 30px 20px;
  z-index: 10;
  color: #26a699;
}
.zona1 {
  position: relative;
  background-image: url(assets/7.jpg);
  width: 100%;
  height: 600px;
  background-size: cover;
  background-position: center center;
  opacity: 0.8;
}
section button {
  background-color: #fff;
}
header.abajo {
  background: #26a699;
  padding: 5px 10px;
}
header.abajo {
  color: #fff;
}
header img {
  width: 100px;
  height: 45px;
}
#phonebtn {
  margin-top: -20px;
}

.menu-nav {
  display: flex;
  padding: 1rem;
}
.nav-list {
  list-style-type: none;
  display: flex;
  gap: 1rem;
}
.open-menu,
.closed-menu {
  display: none;
}
.list_item {
  cursor: pointer;
}
.my-menu-link {
  color: white;
  border-bottom: 5px solid white;
}

@media screen and (max-width: 780px) {
  .open-menu,
  .closed-menu {
    display: block;
    color: white;
  }
  .list_item {
    cursor: pointer;
  }
  .my-menu-link {
    color: white;
    border-bottom: 5px solid white;
  }
  .nav {
    opacity: 0;
    visibility: hidden;
  }
  .nav {
    display: flex;
    flex-direction: column;
    align-items: end;
    gap: 1rem;
    position: fixed;
    bottom: 0;
    top: 0;
    right: 0;
    padding: 2rem;
    background-color: #1c1c1c;
    box-shadow: 0 0 0 100vmax rgba(0, 0, 0, .5);
  }
  .nav.visibility {
    opacity: 1;
    visibility: visible;
  }
  .nav-list {
    flex-direction: column;
    align-items: end;
  }
}
</style>
