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
          <span class="nav-bar" id="btnMenu" icon="ti-align-justify">Menu</span>
          <q-nav class="main-nav">
            <ul class="menu" id="menu">
              <li class="menu__item"><a href="" class="menu__link">Inicio</a></li>
              <li class="menu__item"><a href="" class="menu__link">Sobre Nosotros</a></li>
              <li class="menu__item container-submenu">
                <a href="" class="menu__link">Lista de Animales</a>
                <ul class="submenu">
                  <li class="menu__item"><a href="" class="menu__link">Adoptar</a></li>
                  <li class="menu__item"><a href="" class="menu__link">Visitar</a></li>
                </ul>
              </li>
              <li class="menu__item"><a href="" class="menu__link">Contactenos</a></li>
            </ul>
          </q-nav>
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

const btnMenu = ref(null);
const menu = ref(null);

const toggleMenu = () => {
  menu.value.classList.toggle('mostrar');
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
header.abajo button {
  color: #fff;
}
header img {
  width: 100px;
  height: 45px;
}
#phonebtn {
  margin-top: -20px;
}

.nav-bar {
  background: #26a69a;
  padding: 20px;
  display: block;
  color: white;
  cursor: pointer;
  font-size: 1.5em;
  width: 100%;
}
.menu, submenu {
  list-style: none;
  padding: 0;
  margin: 0;
}
.menu {
  background: #555;
  width: 100%;
  margin-left: -110%;
}
.menu__link {
  display: block;
  padding: 20px;
  color: white;
  font-size: 1.4em;
  text-decoration: none;
}
.menu__link:hover {
  background: #26a69a;
}
.submenu .menu__link:hover {
  background: #222;
}
.submenu {
  height: 0;
  overflow: hidden;
  transition: all 0.3s;
}
.submenu .menu__link {
  background: #333;
  padding-left: 50px;
}
.mostrar {
  margin-left: 0;
}

@media(min-width:1024px) {
  .nav-bar {
    display: none;
  }
  .menu {
    margin-left: 0;
    display: flex;
  }
  .container-submenu {
    position: relative;
  }
  .submenu {
    position: absolute;
    top: 70px;
    width: 200px;
    overflow: visible;
    z-index: 1000;
    opacity: 0;
    visibility: hidden;
  }
  .container-submenu:hover .submenu {
    opacity: 1;
    visibility: visible;
  }
}
</style>
