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
   <tbody>
      <tr >
         <td>1</td>
         <td>2</td>
         <td>3</td>
         <td>5</td>
      </tr>
   </tbody>
</table>
</template>

<script>
export default{
name: 'ComponentTable',
}
</script>

<style>
table {
    width: 50%;
    margin-top: 50px;
    margin-left: 25%;
    margin-right: 25%;
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