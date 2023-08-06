<template>
  <div class="row justify-center q-pt-md">
    <div class="col-10 bg-secondary" id="seccion4">
      <div class="row justify-center">
        <div class="col-8 flex flex-center q-pa-xl">
          <h3>Siganos para mas Informacion</h3>
          <p>
            Deje su correo electronico y nosotros le enviaremos mas informacion
            sobre actividades que realicemos o temas sobre la ayuda a los
            animalitos. Debidamente entrenado, el hombre puede llegar a ser el
            mejor amigo del perro.
          </p>
          <input v-model="text" rounded label="Escriba su Correo" />
          <q-btn label="Enviar" rounded id="enviar" />
        </div>
      </div>
    </div>
  </div>
</template>

<style>
#seccion4 {
  border-radius: 20px;
  color: white;
}
#seccion4 h3 {
  font-size: 36px;
}
div input {
  border: none;
  border-radius: 20px;
  width: 500px;
  height: 45px;
  color: #26a69a;
}
#enviar {
  margin-left: -90px;
  background-color: #26a69a;
}
</style>
