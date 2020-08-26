<template>
   <div class="formProps mt-4">
      <b-row>
         <b-col sm="12">
            <h1 class="mb-4">{{msg}}</h1>
            <b-form-input id="input-default" v-model="newTask" @keyup.enter="addTask" placeholder="Ingresa una actividad"></b-form-input>
         </b-col>
      </b-row>
      <b-row>
         <b-col sm="12" class="mt-4">
            <b-button variant="success" @click="addTask" class="mx-4">Agregar</b-button>
            <b-button variant="danger"  @click="clearList" class="mx-4">Limpiar</b-button>
         </b-col>
         <b-col sm="12" class="my-4">
            <childProps :array="arrayList" @deleteItem="remove($event)" />
         </b-col>
      </b-row>
   </div>
</template>

<script>
import childProps from './childProps';

export default {
  name: 'props',
  components: { childProps },
  props: {
    msg: String
  },
  data() {
      return {
        newTask: '',
        arrayList: []
      }
  },
  methods: {
     addTask() {
        this.arrayList.push(this.newTask);
        this.newTask = '';
     },
     remove(index) {
        this.arrayList.splice(index, 1)
     },
     clearList() {
        this.arrayList = [];
     }
  }
}
</script>