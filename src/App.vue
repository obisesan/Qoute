<template>
  <div id="app">
   <Header :qouteCount="quotes.length " :maxQoute="maxQoute" ></Header>
   <NewQoute @qouteAdded="NewQoute"></NewQoute>
   <QuoteGrid :quotes="quotes" @quoteDelete="deleteQuote"></QuoteGrid>
  
   <div class="col-sm-12 text-center">
     <div class="alert alert-info">Info: Click on a Quote to Delete it</div>
   </div>
  </div>
</template>

<script>
 import QuoteGrid  from './components/QuoteGrid.vue'
 import NewQoute  from './components/NewQoute.vue'
 import Header  from './components/Header.vue'
export default {
  name: 'App',
  data:function(){
    return{
       quotes:[
         "JUst have something to Somethiing ",
       ],
       maxQoute:30,
    }
  },
  methods:{
      NewQoute(quote){
        if(this.quotes.length >= this.maxQoute){
          return  alert("Please! , Delete a Quote");
        }
        this.quotes.push(quote)
      },
      deleteQuote(index){
        this.quotes.splice(index,1)
      }
  },
 components:{
   QuoteGrid:QuoteGrid,
   NewQoute:NewQoute,
   Header:Header
 }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
