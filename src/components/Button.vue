<template>
    <button @click="onClick()" :style="{ background: color}">{{title}}</button>
</template>

<script>
    export default {
        name: 'Button',
        props: {
            title: String,
            color: String,
        },
        methods: {
            onClick() {
                console.log('You just clicked me....');
            }
        }
    }
</script>