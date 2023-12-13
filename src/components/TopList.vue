<script>
import TopItem from './TopItem.vue';

export default {
    components: {
        TopItem
    },
    name: 'TopList',
    props: ['pairs'],
    data() {
        return {
            top: 0
        };
    },
}
</script>

<template>

        <div class="css-k2osh3"></div>
        <div class="css-10id09q">
            <p class="chakra-text css-ax34ea">Trending</p>
        </div>
        <div class="css-xamd77">
            <div class="css-qm29w9">
                <a v-for="pair in pairs">
                    <TopItem v-bind:pair="pair" :top=++top></TopItem>
                </a>
            </div>
        </div>

</template>

<style scoped>
.css-qm29w9 {
    display: flex;
    -webkit-box-align: center;
    align-items: center;
    flex-wrap: nowrap;
    gap: var(--chakra-space-4);
    width: 100%;
}

.css-xamd77 {
    overflow-x: auto;
    margin-right: var(--chakra-space-8);
    flex: 1 1 0%;
}

.css-10id09q {
    display: flex;
    -webkit-box-align: center;
    align-items: center;
    font-weight: 600;
    gap: var(--chakra-space-1);
}

.css-ax34ea {
    display: flex;
}

.css-k2osh3 {
    display: flex;
    -webkit-box-align: center;
    align-items: center;
    flex: 1 1 0%;
    padding-top: var(--chakra-space-3);
    padding-bottom: var(--chakra-space-3);
}

.css-137m7ew {
    display: flex;
    flex-direction: column;
    padding-inline-start: var(--chakra-space-2);
    padding-inline-end: var(--chakra-space-2);
    background: rgb(251, 252, 253);
    font-size: var(--chakra-fontSizes-xs);
    position: static;
    top: 56px;
    z-index: 998;
    height: 48px;
}
</style>
