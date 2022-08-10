<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    
    <label for="">Numero 1   </label>
    <input type="Number" v-model="nro1" placeholder="Indique el Numero 1">
    <br><br><br>
    
    <label for="">Numero 2   </label>
    <input type="Number" v-model="nro2" placeholder="Indique el Numero 2">
    <br><br><br>
    
    <label for="">Operacion   </label>
    <select v-model="selected">
      <option  v-for="item in operations" :value="item" :key="item.id">
        {{ item.name }}
      </option>
    </select>
    <br><br><br>
    
    <button @click="calcular()">Calcular</button>
    <br><br>
    
    <label >Resultado    </label>
    <input type="Number" v-model="result" placeholder="El resultado es" disabled>



  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data: () => ({
    nro1: " ",
    nro2: " ",
    result: " ",
    operations: [
      {id: 1, name: 'Suma'},
      {id: 2, name: 'Resta'},
      {id: 3, name: 'Multiplicacion' },
      {id: 4, name: 'Division' }
    ],
    table: '',
  }),
  props: {
    msg: String
  },
  methods: {
    calcular(){
      if(this.selected.id === 1){
        this.result= Number(this.nro1) + Number(this.nro2)
      }
      else
      {
        if (this.selected.id === 2){
          this.result= Number(this.nro1) - Number(this.nro2)
        }
        else{
          if (this.selected.id === 3){
            this.result= Number(this.nro1) * Number(this.nro2)
          }
          else 
          this.result= Number(this.nro1) / Number(this.nro2)
      } 
      }      
    }
  }
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>

input, select{
  width: 150px;
  height: 40px;
  background-color: rgb(219, 245, 232);
  box-sizing: border-box;
  border: 2px solid rgb(21, 241, 113);
  border-radius: 4px;
}

button{
    width: 100px;
    height: 40px;
    border-radius: 10px;
    background-color: aliceblue;
    border-color: rgb(9, 243, 141);
    text-align: center;
    transition-duration: 0.5s;
}

button:hover{
    background-color: #4CAF50; /* Green */
    color: white;
    
}

label{
    font-family: Avenir, Helvetica, Arial, sans-serif;
    color: rgb(2, 31, 11);
    text-decoration: solid;
}
</style>
