<template>
    <div class="row">
        <app-quote v-for="(quote, index) in quotes" @click.native="updateMe(index)">{{quote}}</app-quote>
    </div>
</template>
<script>
    import Quote from './Quote.vue';
    export default{
        props: ['quotes'],
        components:{
            appQuote: Quote
        },
        methods:{
            updateMe(index){
                this.$emit('quoteUpdated', index);
            }

        }
    }
    
</script>

<style>

</style>
