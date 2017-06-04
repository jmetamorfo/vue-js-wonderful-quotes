<template>
  <div class="row">
    <div class="col-xs-4 form-group">
      <form>
        <label>Quote:</label>
        <textarea class="form-control col-xs-3" rows="3" v-model="quote"></textarea>
      </form>

      <div class="col-xs-12 form-group">
        <button class="btn btn-primary" @click.prevent="createNew">Add Quote</button>
      </div>

    </div>
  </div>
</template>

<script>

  export default {
      data: function() {
        return {
          quote: ''
        };
      },
      methods: {
        createNew() {
          this.$emit('quoteAdded', this.quote);
          this.quote = '';
        }
      }
  }
</script>