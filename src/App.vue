<template>
  <div class="container">

    <app-new-quote @quoteAdded="newQuote"></app-new-quote>
    <app-quote-grid :quotes="quotesArray"></app-quote-grid>
      
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
