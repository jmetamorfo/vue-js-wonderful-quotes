<template>
    <div class="container">
      <app-quote-grid :quotes="quotesArray"></app-quote-grid>
    </div>
</template>

<script>
  import QuoteGrid from './components/QuoteGrid.vue';

  export default {
    data: function() {
      return {
        quotesArray: [
          'Just a Quote to see something'
        ],
        maxQuotes: 10
      };
    },
    components: {
      appQuoteGrid: QuoteGrid
    }
  }
</script>

<style>
</style>
