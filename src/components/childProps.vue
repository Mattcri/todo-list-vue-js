<template>
   <div>
      <ul>
         <li v-for="(item, index) in array" :key="index">{{item}}
             <b-button pill variant="outline-danger" @click="$emit('deleteItem', index)">
                <b-icon icon = "x-circle" variant = " danger " > </b-icon>
             </b-button>
         </li>
      </ul>
   </div>
</template>

<script>
export default {
  name: 'childProps',
  props: {
    array: Array
  },
//   data() {
//      return {

//      };
//   },
//   methods: {

//   }
}
</script>

<style scoped>
ul {
   list-style: none;
   padding: 0 5px;
}
li {
   display: flex;
   justify-content: space-between;
   align-items: center;
   margin: 10px 0;
}


</style>