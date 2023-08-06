<template>
  <q-page>
    <div class="row justify-center q-pt-xl">
      <div class="col-12 col-sm-6 col-md-8">
        <h3 style="color: #26a69a">Animales Disponibles para Ayudar</h3>
      </div>
    </div>
    <div class="row justify-center q-pt-md">
      <div class="col-12 col-sm-6 col-md-3 flex flex-center">
        <q-card class="my-card">
          <img src="~assets/3.png" />

          <q-card-section>
            <div class="text-h6">Labrador</div>
            <div class="text-subtitle2">Edad: 6 Meses</div>
            <q-btn icon="add" label="Adoptar" style="color: #26a69a" />
          </q-card-section>
        </q-card>
      </div>
      <div class="col-12 col-sm-6 col-md-3 flex flex-center">
        <q-card class="my-card">
          <img src="~assets/4.jpg" />

          <q-card-section>
            <div class="text-h6">Gato</div>
            <div class="text-subtitle2">Edad: 1 Año</div>
            <q-btn icon="add" label="Adoptar" style="color: #26a69a" />
          </q-card-section>
        </q-card>
      </div>
      <div class="col-12 col-sm-6 col-md-3 flex flex-center">
        <q-card class="my-card">
          <img src="~assets/pastor.jpg" />

          <q-card-section>
            <div class="text-h6">Pastor Aleman</div>
            <div class="text-subtitle2">Edad: 12 Años</div>
            <q-btn icon="add" label="Adoptar" style="color: #26a69a" />
          </q-card-section>
        </q-card>
      </div>
    </div>
    <div class="contenedor-acordeon" id="listado">
      <div class="acordeon">
        <input
          type="radio"
          name="acordeon"
          id="btn-acordeon1"
          class="btn-acordeon"
        />
        <label for="btn-acordeon1" style="color: #26a69a"
          >Mostrar Mas Animales</label
        >
        <div class="contenido-acordeon flex flex-center">
          <q-card class="my-card">
            <img src="~assets/7.jpg" />

            <q-card-section>
              <div class="text-h6">Visite la</div>
              <div class="text-subtitle2">Lista de Animales para ver mas</div>
              <q-btn icon="add" label="Visitar" style="color: #26a69a" />
            </q-card-section>
          </q-card>
        </div>
      </div>
    </div>
  </q-page>
</template>

<style>
@import url("https://fonts.googleapis.com/css2?family=Raleway:wght@400;800&display=swap");
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Raleway", sans-serif;
}
.contenedor-acordeon {
  width: 100%;
  max-width: 800px;
  margin: auto;
  margin-top: 0px;
}
.contenedor-acordeon h2 {
  text-align: center;
  font-size: 40px;
  margin-bottom: 35px;
}
.acordeon {
  background: #fff;
}
.acordeon label {
  display: block;
  padding: 20px;
  font-size: 20px;
  background: #1c1c1c00;
  color: rgb(7, 6, 6);
  cursor: pointer;
  margin-bottom: 2px;
  transition: all 300ms ease;
}
.acordeon label:hover {
  background: #f1eded;
}
.acordeon .contenido-acordeon {
  padding: 0px;
  margin: 0px 20px;
  max-height: 0px;
  overflow: hidden;
  transition: all 300ms ease;
}
.btn-acordeon:checked ~ .contenido-acordeon {
  max-height: 600px;
  padding: 15px 0px;
}
.btn-acordeon {
  display: none;
}
div img {
  padding: 5px;
  width: 200px;
  height: 200px;
}
</style>
