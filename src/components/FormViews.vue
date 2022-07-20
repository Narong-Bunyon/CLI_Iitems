<template>
  <form class="forms">
  <input type="text" class="first" placeholder="First-Name" v-model="firstName"><br>
  <input type="text" class="last" placeholder="Last-Name" v-model="lastName"><br>
  <input type="text" class="comment" placeholder="comments" v-model="comment"><br>
  <div class="butt">
    <button class="addButton" @click="addItem">Add</button>
  </div>


</form>
<Cardstore :cards="fullName"/>

</template>

<script>
import     Cardstore from './CardStoreViews.vue'
export default {
  components:{

    Cardstore



  },

  data(){
    return{
      fullName:[],
      firstName:'',
      lastName:'',
      comment:''
    }

  },
methods:{
    addItem(event){
      event.preventDefault()
      let object={};

      object.firstnames=this.firstName;
      object.lastnames= this.lastName;
      object.comments=this.comment;
      this.fullName.push(object);
      console.log(this.fullName)
      this.firstName="";
      this.lastName="";
      this.comment="";

    }


  }
 

}


</script>

<style>

.first,.last,.comment{
    width: 700px;
    height: 4vh;
    margin: 5px 5px;
    font-size: 18px;
}
.adds{
  padding: 5px 5px;
  margin: 10px 10px;
  font-size: 20px;
}

.butt{
  margin: auto;
  justify-content: center;
  display: flex;
}

.addButton{
  height: 4vh;
  width: 400px;
  border: 1px solid red;
  border-radius: 4px;
  background: teal;
  color: white;
  margin: 10px 10px;
  display: flex;
  font-size: 20px;
  text-align: center;
  align-items: center;
  justify-content: center;
  
}



</style>