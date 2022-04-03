<template>
<form action="Post">
<div class="row">
    <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
        <label for="Quote">Quote</label><br>
        <textarea name="" id="form" class="form" cols="50" rows="3" v-model="qoute"></textarea>
    </div>
    <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
       <button class="btn btn-primary" @click.prevent="createNew">Add Quote</button>
    </div>
    </div>
    </form>
</template>
<script>
export default {
    data: function (){
        return{
            qoute: ""
        }
    },
    methods:{
       createNew(){
         this.$emit("qouteAdded", this.qoute);
         this.qoute = "";
       }
    }
}
</script>
<style scoped>

</style>