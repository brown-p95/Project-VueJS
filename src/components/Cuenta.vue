<template>
<div>
  <h2><hr/>Tipo de cuenta: {{account}}</h2>
  <h2><hr/>Saldo: {{balance}}</h2>
  <h2><hr/>Cuenta: {{status ? 'Activa' : 'Desactivada'}}</h2>
  <h3><hr/><div v-for="(item,index) in servicios" :key="index">
  {{index+1}} - {{item}}
  </div></h3>
  <AccionBalance 
    text="Aumentar saldo"
    @accion="add"
    
  />
  <AccionBalance 
    text="retirar todo"
    @accion="remove_all"
    :disabled="disabledp"
  />
  <AccionBalance 
    text="Disminuir saldo"
    @accion="subtract"
    :disabled="disabledp"
  />
  </div>
</template>

<script>
import AccionBalance from './AccionBalance.vue';
export default {
    
      components: {
        AccionBalance
      
    },
    data() {
        return {
            disabledp:false,
            balance: 1000,
            account: "Visa",
            status: true,
            servicios: ["Tranferencia", "Pago de servicio", "Factura"]
        };
    },
    methods: {
      add(){
        this.balance +=100;
        this.disabledp=false
      },
      subtract(){
        if(this.balance===0){
          alert('no hay saldo')
          this.disabledp=true
        }
        else{
        this.balance -=100;
        }
      },
       remove_all(){
        alert('se retiro todo '+this.balance)
        this.balance = 0
        this.disabledp=true
        }

    }
}
</script>

<style scoped>
 h1{
  background-color: palegreen;
    color: blue;
 }
</style>