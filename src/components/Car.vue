<template>
  <h3>Componentes del auto (api de composicion)</h3>
  <p>Marca: {{ brand }}</p>
  <p>Modelo: {{ model }}</p>
  <p>Potencia: {{ power }}</p>
  <button @click="upPower">Aumentar</button>
  <button @click="downPower">Disminuir</button>
  <!-- no hace falta mas que agregar el nombre de la variable para
  poder traer y mostrar a travez de los props -->
  <!-- <button @click="upPower(10)">Aumentar</button> - <button @click="downPower(5)">Disminuir</button> -->
</template>

<script>
import { ref } from 'vue'
export default {
  props: {
    power: {
      type: Number,
      default: 60,
    },
    upPower: Function, 
    downPower: Function,// esto llama la funcion decladara en  app.vue
  },
  setup(props){
    const brand="Cupra";
    const model="xf5";
    console.log(props);
    // let power= ref(40);

    // const upPower = (newPower) => {
    //   console.log("Aumentar potencia component");
    //   power.value = power.value + newPower
    //   console.log(power.value + " Aumenta de a 10")
    // };
    // const downPower = (newPower) => {
    //   // console.log("Bajar potencia component" + newPower)
    //   power.value = power.value - newPower
    //   console.log(power.value + " resta de a 5")
    // }
    
    return{
      brand, model, 
    
      
    };
  },

}
</script>

<style>

</style>