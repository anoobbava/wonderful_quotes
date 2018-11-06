<template>
    <div class="row">
        <form>
            <div class="col-sm8-col-sm-offset-2 form-group">
                <label>new Quote</label>
                <textarea class="form-control" cols="10" rows="3" v-model="quote"></textarea>
            </div>
            <div class="col-sm8-col-sm-offset-2 form-group">
                <button class="btn btn-primary" @click.prevent="addQuote">Add Quote</button>
            </div>
        </form>
    </div>
</template>
<script>
    export default{
        data(){
            return{
                quote: ''
            }
        },
        methods:{
            addQuote(){
                this.$emit('quoteAdded',  this.quote);
                this.quote = '';
            }
        },
        components: {

        }
    }
    
</script>

<style>
    
</style>
