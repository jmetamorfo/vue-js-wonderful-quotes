<template>
  <div class="container">

    <app-new-quote @quoteAdded="newQuote"></app-new-quote>
    <app-quote-grid :quotes="quotesArray" @quoteDeleted="deleteQuote"></app-quote-grid>
    <div class="row">
      <div class="col-xs12 text-center">
        <div class="alert alert-info">
          Info: Click in a quote to delete it.
        </div>
      </div>
    </div>

    </div>
</template>

<script>
  import QuoteGrid from './components/QuoteGrid.vue';
  import NewQuote from './components/NewQuote.vue';

  export default {
    data: function() {
      return {
        quotesArray: [
          'Just a Quote to see something'
        ],
        maxQuotes: 10
      };
    },
    methods: {
      newQuote(quote) {
        this.quotesArray.push(quote);
      },
      deleteQuote(index) {
        this.quotesArray.splice(index, 1);
      }
    },
    components: {
      appQuoteGrid: QuoteGrid,
      appNewQuote: NewQuote
    }
  }
</script>

<style>
</style>
