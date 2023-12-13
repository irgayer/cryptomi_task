<script>
export default {
    name: 'TopItem',
    props: ['pair', 'top'],
}
</script>

<template>
    <!-- <div class="css-wd8hou">
        <p>#{{ top }}</p>
        <p> {{ pair.symbol }}</p>
        <img src="../assets/ethereum.webp">
    </div> -->
    <a class="chakra-link css-hcs0of">
        <div class="css-trdxez">
            <p class="chakra-text css-0" style="color: {{ (top <= 3) ? yellow : black }}">#{{ top }}</p>
            <p class="chakra-text css-10apc93">{{ pair.symbol }}</p><img alt="{{ pair.symbol }}" class="chakra-image css-1vi1txg"
                src="../assets/ethereum.webp">
        </div>
    </a>
</template>

<style scoped>
a {
    background-color: transparent;
    color: inherit;
    text-decoration: inherit;
}
.css-hcs0of {
    transition-property: var(--chakra-transition-property-common);
    transition-duration: var(--chakra-transition-duration-fast);
    transition-timing-function: var(--chakra-transition-easing-ease-out);
    cursor: pointer;
    text-decoration: none;
    outline: transparent solid 2px;
    outline-offset: 2px;
    color: inherit;
    font-size: var(--chakra-fontSizes-sm);
    display: inline-block;
    min-width: max-content;
}

.css-trdxez {
    display: flex;
    -webkit-box-align: center;
    align-items: center;
    gap: var(--chakra-space-1);
    color: var(--chakra-colors-yellow-400);
}

.css-10apc93 {
    white-space: nowrap;
    text-transform: uppercase;
}

.css-1vi1txg {
    width: 20px;
    height: 20px;
    border-radius: 100%;
}
</style>