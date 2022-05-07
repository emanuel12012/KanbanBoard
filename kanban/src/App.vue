<template>
  <div class="contaioner mt-5"
    <div class="row">
     <div class="col form-inline">
        <b-form-input v-model="newTask" placeholder="Enter Task" @keyup.enter="add"></b-form-input>
      </div>
    </div>
  </div>
</template>

<script setup>
import draggable from "vuedraggable";
name: 'App',
components; {
  draggable
},
data(){
  return {
    newTask: "",
    arrBacklog: [
      {name: "Code Sign Up Page"},
      {name: "Test Dashboard"},
      {name: "Style Registation"},
      {name: "Helo with Designs"},
    ],
    arrInProgress:[],
    arrTested:[],
    arrDone: []
  }
},
methods:{
  add() {
    if(this.newTask) {
      this.arrBacklog.push({name: this.newTask  });
      this.newTask="";
    }
  }
}
</script>

<style>
</style>