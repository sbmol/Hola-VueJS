<template>
  <Car :power="power" :upPower="upPower" @downPower="downPower"/> <!-- para decir a vue que es una variable tenemos que poner los 
  puntos para poder hacer correctamente los props, las funciones para pasar como custom emmit usar el
arroba-->
  <hr>


  <hr>
  
  <!-- <h1>Nuestro primer componente</h1>
  
  <h3>ESTO ES API DE OPCIONES</h3>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{  model }}</p>
  <p>PRECIO: {{ price }}</p>
  <p>power: {{ power }}</p>
  <p>color: 
    <ul>
      <li v-for="(color, index) in colors" :key="index">
        {{ index }}: {{ color }}
      </li>
    </ul>
  </p>
  <p>Mensaje: {{ message.title }}, {{ message.text }}</p>
  <h3>Esto es API DE COMPOSICION</h3>
  <p>Datos de Vehiculo {{ branded }} - {{ model1 }} - {{ engine }} - {{ power1 }} - mensaje: {{ message1.title2 }}</p>
  <If /> -->
</template>

<script>
import { ref } from 'vue'
import Car from './components/Car.vue'

export default {
  components: {
     Car,
    //  CarOptions,
  },
  setup(){
    let power = ref(30);

    const upPower = () => {
      power.value++;
      console.log("Aumentar power...")

    }
    const downPower = () => {
      power.value--;
      console.log("Reduciendo..")
    }


    return {
      power,
      upPower,
      downPower,
    };
  },
  // API DE OPCIONES
  // data(){
  //   return{
  //     brand: "Audi",
  //     model: "A4",
  //     price: "20000",
  //     power: "190",
  //     colors: ["azul", "rojo", "verde", "amarillo"],
  //     message: {
  //       title: "Nuevo en Promocion!",
  //       text: "Aprovecha esta oportunidad unica!"
  //     }
  //   };
    
  // },
  // API COMPOSICION
  // setup(){
  //   const branded = "Hyundai";
  //   const model1 = "Accent";
  //   const engine = "1500";
  //   const price1 = "45000";
  //   const power1 = "240";
  //   const message1 = {
  //     title2: "hola",
  //     text2: "eu",
  //   }
  //   return{
  //     branded, model1, price1, engine, power1, message1
  //   }
  // }

};
</script>

<style>

</style>