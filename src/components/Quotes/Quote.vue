<template>
    <div class="quote">
        <slot></slot>
    </div>
</template>

<script>
export default {
    props: ['quote']
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
