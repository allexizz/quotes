<template>
    <div class="container">
        <quote-header :count="quotes.length" :maxQuotes="maxQuotes"></quote-header>
        <new-quote @quoteCreated="createQuote"></new-quote>
        <quote-grid :quotes="quotes" @quoteDeleted="deleteQuote"></quote-grid>
        <div class="row">
            <div class="text-center">
                <div class="alert alert-info">Click on quote to delete it</div>
            </div>
        </div>
    </div>
</template>

<script>
import QuoteGrid from './components/Quotes/QuoteGrid.vue';
import NewQuote from './components/Quotes/NewQuote.vue';
import Header from './components/Shared/Header.vue';

    export default {
        data: function() {
            return {
                quotes: [],
                maxQuotes: 10
            }
        },
        components: {
            QuoteGrid: QuoteGrid,
            NewQuote: NewQuote,
            QuoteHeader: Header
        },
        methods: {
            createQuote(quote) {
                if (this.quotes.length >= this.maxQuotes) {
                    return alert('Delete quote first');
                }
                this.quotes.push(quote);
            },
            deleteQuote(index) {
                this.quotes.splice(index, 1);
            }
        }
    }
</script>