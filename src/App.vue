<script>

import axios from 'axios';
import {store} from './data/store';

  export default{
    
    name: 'App',
    data(){
      return{
        title:'Welcome'
      }
    },
    methods:{
      getApi(){
        axios.get(store.apiUrl + 'projects')
        .then(results=>{
          console.log(results.data);
        })
      }
    },
    mounted(){
      this.getApi();
    }
  }
</script>

<template>
  
  <div>
    <h1>{{title}}</h1>
  </div>
</template>

<style lang="scss" scoped>

</style>
