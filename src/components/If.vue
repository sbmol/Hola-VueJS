<template>
  <h2>Hola desde IF</h2>
  <p> Marca: {{ marca }}</p>
  <p>Año: {{  year }}</p>
  <p>Motores menores a 300 cv: 
    <!-- <ul>
      <li v-for="(motor, index) in motores" :key="index">
        <span v-if="motor < 300">
          {{ motor }}
        </span>
      </li>
    </ul> -->
  </p>
  <!-- PRIMERO VA EL IF, ELSE-IF, LUEGO EL ELSE-->
  <template v-for="(motor, index) in motores" :key="index">
  <li v-if="motor < 175">
    Urbana: {{ motor }}
  </li>
  <li v-else-if="motor === 180">
    Hibrido: {{ motor }}
  </li>
  <li v-else="motor > 350">
    Carrera: {{ motor }}
  </li>
 
 </template>
 

</template>

<script>
export default {
  // ahora vamos a ver las condiciones v-if 
  setup(){
    const marca = "Toyota";
    const year = "1995";
    const motores = [60, 120, 140, 175, 180, 200, 220, 300, 350, 550];
    return{
      marca, year, motores,
    }
  }
  

}
</script>


<style>

</style>