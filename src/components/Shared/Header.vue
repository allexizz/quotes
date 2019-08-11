<template>
    <div class="row">
    <h3>Quotes added</h3>
    <div class="progress">
        <div class="progress">
            <div class="progress-bar" role=progressbar aria-valuenow="60" aria-valuemax="100" aria-valuemin="0"
                :style="{width: (count / maxQuotes) * 100 + '%' }">
                {{count}} / {{maxQuotes}}
            </div>
        </div>
    </div>
    </div>
</template>

<script>
export default {
    props: ['maxQuotes', 'count']
}
</script>
<style>
    .quote {
        width: 350px;
        height: 150px;
        cursor: pointer;
        margin-top: 20px;
        font-size: 28px;
        border: 1px solid black;
        text-align: center;
    }

    .quote:hover {
        background-color: burlywood;
    }
</style>
