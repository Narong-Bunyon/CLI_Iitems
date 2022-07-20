<template>
  <div class="cardsStore" v-for="card of cards" :key="card">
    <div class="cardon">
      <div class="firstName">{{card.firstnames }} {{card.lastnames}}</div>
      <div class="Comments">{{card.comments}}</div>
    </div>
  </div>
</template>

<script>


export default {

  props:{
    cards:[]
  },

components:{
  
}
 
}
</script>

<style>

.cardsStore{
  margin: auto;
  display: flex;
  width: 450px;
}
.cardon{
  width: 500px;
  
  border-radius: 10px;
  margin: 10px 10px;
  border: solid 2px purple;
  border-style:dotted;
  
}
.firstName,.Comments{
  text-align: center;
  display: flex;
  padding: 10px 10px;
  margin: 5px 5px;
}

</style>