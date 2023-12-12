<template>
  <h4>Opciones del auto (api de opciones)</h4>
  <p>Marca: {{ brand }}</p>
  <p>Model: {{ model }}</p>
  <p>Power: {{ power }}</p>
  <button @click="upPower"> Aumentar </button> - <button @click="downPower"> Disminuir</button>
</template>

<script>
export default {
  data(){
    return{
      brand: "Seat",
      model: "Leon",
      power: 60,
    }
  },
  methods:{
    upPower(){
      // console.log("Aumentando potencia", + this.power)
      // this.power = this.power + 10;
      this.power++;
    },
    downPower(){
      // console.log("Quitando potencia", + this.power)
      // this.power = this.power - 5;
      this.power--;
    }
  }

}
</script>

<style>

</style>