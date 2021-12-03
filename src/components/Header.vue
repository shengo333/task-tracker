<template>
    <header>
        <h1>{{title}}</h1>
        <Buttton @btn-click="$emit('toggle-add-task')" 
        :text="showAddTask ? 'Close':'Add Task'" 
        :color="showAddTask ? 'red':'green'"/>
    </header>
</template>

<script>
import Buttton from './Buttton.vue'

export default {
    name: 'Header',
    props: {
        title: String,
        showAddTask: Boolean
    },
    components: {
        Buttton,
    },
}
</script>

<style scoped>
    header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 20px;
    }
</style>