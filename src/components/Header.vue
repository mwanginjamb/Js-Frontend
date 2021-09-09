<template>
    <header>
        <h1>{{ title }}</h1>
        <Button 
         @btn-click="$emit('toggle-form')"
         class="btn"
         :state="showAddTask"
         :color="showAddTask ? 'red' : 'green' " 
         :title="showAddTask ? 'Close' : 'Add Task' " />
    </header>
    
</template>




<script>
import Button from './Button.vue'
export default {
   
    name: 'Header',
    components: {
        Button
    },
    props: {
        title: String,
        showAddTask: Boolean
    }
    
}
</script>

<style scoped>
    header {
        display: flex;
        justify-content: space-around;
        align-items: center;
        margin-bottom: 20px;
    }
</style>