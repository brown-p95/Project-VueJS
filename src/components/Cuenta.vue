<template>
  <h2><hr/>Tipo de cuenta: {{account}}</h2>
  <h2><hr/>Saldo: {{balance}}</h2>
  <h2><hr/>Cuenta: {{status ? 'Activa' : 'Desactivada'}}</h2>
  <h3><hr/><div v-for="(item,index) in servicios" :key="index">
    {{ item+1}}+{{item}}
  </div></h3>
</template>

<script>
export default {
    data(){
        return{
        balance:1000,
        account:'Visa',
        status:true.valueOf,
        servicios:['Tranferencia','Pago de servicio','Factura']

        }
    }
}
</script>

<style>
 h1{
  background-color: palegreen;
    color: blue;
 }
</style>