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
    <div class="">
        <a v-for="pair in pairs">
            <TopItem v-bind:pair="pair" :top=++top></TopItem>
        </a>
    </div>
</template>