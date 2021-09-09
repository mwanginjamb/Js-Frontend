<template>
    
    <button @click="onClick()" :style="{ background: color}">
        <i v-if="!state" class="fa fa-plus-circle"></i>
        <i v-if="state" class="fa fa-minus-circle"></i>

         {{title}}</button>
</template>

<script>
    export default {
        name: 'Button',
        props: {
            title: String,
            color: String,
            state: Boolean
        },
        methods: {
            onClick() {
                this.$emit('toggle-form');
            }
        }
    }
</script>