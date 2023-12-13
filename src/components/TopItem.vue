<script>
export default {
    name: 'TopItem',
    props: ['pair', 'top'],
}
</script>

<template>
    <div class="css-wd8hou">
        <p>#{{ top }}</p>
        <p> {{ pair.symbol }}</p>
        <img src="../assets/ethereum.webp">
    </div>
</template>

<style scoped>
.css-wd8hou {
    display: flex;
    -webkit-box-align: center;
    align-items: center;
}
</style>