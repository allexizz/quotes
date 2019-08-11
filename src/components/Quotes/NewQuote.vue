<template>
    <div class="new-quote">
        <form>
            <label class="block-label">Quote: </label>
            <textarea type="text" class="new-quote__input" v-model="quote"></textarea>
            <div>
                <button @click="saveQuote" class="btn btn-primary">Add Quote</button>
            </div>
        </form>
    </div>
</template>

<script>
export default {
    data: function() {
        return {
            quote: ''
        }
    },
    methods: {
        saveQuote(e) {
            e.preventDefault();
            this.$emit('quoteCreated', this.quote);
            this.quote = '';
        }
    }
}
</script>
<style>
    .new-quote__input {
        width: 600px;
        height: 150px;
    }
    
    .block-label {
        display: block;
    }
</style>
