<template>
    <table  class="table">
   <thead>
      <tr>
         <th >Operacion</th>
         <th >Numero 1</th>
         <th >Numero 2</th>
         <th >Resultado</th>
         
      </tr>
   </thead>
   <tbody v-for="item in selectedS" :value="item" :key="item.id">
      <tr>
         <th>{{item.ope}}</th>
         <th>{{item.num1}}</th>
         <th>{{item.num2}}</th>
         <th>{{item.res}}</th>
         
      </tr>
   </tbody>
</table>
</template>

<script>
export default{
name: 'ComponentTable',
props:{
   selectedS:[]
}
}
</script>

<style>
table {  
 width: fit-content;
 margin-top:  10px;

}

tbody{
    background-color: #aeecbd;
    height: 45px;
    
}

thead {
  background-color: #04AA6D;
  color: white;
    text-align: center;
  padding: 8px;
  height: 45px;
}
</style>