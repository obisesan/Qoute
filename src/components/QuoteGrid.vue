<template>
    <div class="row">
       <Quote v-for="(quote,index) in quotes" :key="quote" @click.native="deleteQuote(index)" >{{ quote }} </Quote>
    </div>


</template>
<script>
import Quote from "./Quote.vue"
export default {
    props:['quotes'],
    methods:{
     deleteQuote(index){
         this.$emit("quoteDelete", index)
     }
    },
   components: {
      Quote:Quote
  },
        
       
    
}
</script>
<style scoped>

</style>