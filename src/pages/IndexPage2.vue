<template>
  <q-page>
    <h2>Didacticode</h2>

    <button class="acordeon">Retos</button>
    <div class="panel">
      <p>
        Ponte a prueba afrontando retos de programación junto con Ada y Edu.
        ¡Tienes 10 días para resolverlos antes de conocer la/s respuesta/s!
      </p>
    </div>

    <button class="acordeon">Tips&Tricks</button>
    <div class="panel">
      <p>
        Trucos y consejos para mejorar tu programación, snippets de código
        interesantes, etc.
      </p>
    </div>

    <button class="acordeon">Boleticodes</button>
    <div class="panel">
      <p>
        Consulta todos los boletines de noticias de Didacticode y no te pierdas
        nada :)
      </p>
    </div>
  </q-page>
</template>

<style></style>

<script>
let elementosAcordeon = document.getElementsByClassName("acordeon");

for (let i = 0; i < elementosAcordeon.length; i++) {
  elementosAcordeon[i].addEventListener("click", function () {
    this.classList.toggle("active");
    let panel = this.nextElementSibling;
    if (panel.style.display == "block") {
      panel.style.display = "none";
    } else {
      panel.style.display = "block";
    }
  });
}
</script>
