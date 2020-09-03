<template>
  <div class="container">
    <div>
     
      <h1 class="title">
        sms
      </h1>
        {{counter}}  
 <button class="btn btn-sm btn-info" @click="storetest">store test</button>
      
       
    </div>
  </div>
</template>

<script>

  import{mapState, mapActions,mapGetters} from 'vuex'
    export default {
      computed:{
        ...mapGetters('modules/crudadmin',['counter']),
        // ...mapState('modules/crudadmin',['counter','conter123']),
      },
      methods:{
        
         ...mapActions('modules/crudadmin',['readData']),
        storetest(){
          this.readData({test:'hello'})
        },

      }
        
    }

</script>

<style>

</style> 
