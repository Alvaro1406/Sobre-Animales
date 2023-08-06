<template>
  <q-layout view="hHh lpR fff">
    <q-page-container>
      <router-view />
    </q-page-container>

    <q-footer class="bg-grey-8 text-white">
      <div class="flex flex-center bg-secondary">
        <h3 id="fin">Creado por Jade Soluciones Informaticas</h3>
        <img src="~assets/logo.png" id="finimg" alt="" />
      </div>
    </q-footer>
  </q-layout>
</template>

<style>
#fin {
  font-size: 20px;
}
#finimg {
  width: 100px;
  height: 50px;
}
</style>
