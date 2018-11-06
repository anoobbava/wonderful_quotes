<template>
<div class="container">
  <app-new-quote @quoteAdded='updateQuote'></app-new-quote>
  <app-quote-grid :quotes="quoteData"></app-quote-grid>
  <div class="alert alert-warning col-md-12 alert-note">
    <strong>!!! click on the notes to delete that !!!</strong>
  </div>
</div>
  
</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue';
import NewQuote from './components/NewQuote.vue'

export default {
  data(){
    return{
      maxQuote: 10,
      quoteData: ['this is my test quote']
    }
  },
  methods:{
    updateQuote(data){
      this.quoteData.push(data);
    }
  },
  components: {
    appQuoteGrid: QuoteGrid,
    appNewQuote: NewQuote

  }
}
</script>

<style>
  .alert-note{
    text-align:  center;
  }
  .alert-note:hover{
    color:darkblue;
  
  }
</style>
