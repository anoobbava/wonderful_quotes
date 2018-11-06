<template>
<div class="container">
  <app-header :quoteCount="quoteData.length" :MaxCount="maxQuote"></app-header>
  <app-new-quote @quoteAdded='updateQuote'></app-new-quote>
  <app-quote-grid :quotes="quoteData" @quoteUpdated="deleteQuote"></app-quote-grid>
  <div class="alert alert-warning col-md-12 alert-note">
    <strong>!!! click on the notes to delete that !!!</strong>
  </div>
</div>
  
</template>

<script>
import QuoteGrid from './components/QuoteGrid.vue';
import NewQuote from './components/NewQuote.vue'
import Header from './components/Header.vue'


export default {
  data(){
    return{
      maxQuote: 10,
      quoteData: ['I am the first']
    }
  },
  methods:{
    updateQuote(data){
      if(this.quoteData.length >= this.maxQuote){
        alert('Please delete some data to continue');
      }
      else{
        this.quoteData.push(data);
      }
    },
    deleteQuote(data){
      this.quoteData.splice(data, 1);
    }
  },
  components: {
    appQuoteGrid: QuoteGrid,
    appNewQuote: NewQuote,
    appHeader: Header

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
