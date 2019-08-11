<template>
    <div class="row quotes">
        <quote v-for="(item, i) in quotes" @click.native="deleteQuote(i)">
            <span>{{ item }}</span>
        </quote>
    </div>
</template>

<script>
import Quote from './Quote.vue';

export default {
    props: ['quotes'],
    components: {
        Quote: Quote
    },
    methods: {
        deleteQuote(index) {
            this.$emit('quoteDeleted', index);
        }
    }
}
</script>
<style scoped>
    .quotes {
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
    }
</style>
