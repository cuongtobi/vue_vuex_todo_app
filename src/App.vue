<template>
    <div id="app">
        <div class="container">
            <h1>Todos</h1>
            <AddTodo />
            <Todos />
        </div>
    </div>
</template>

<script>
import Todos from './components/Todos.vue';
import AddTodo from './components/AddTodo.vue'

export default {
    name: 'app',
    components: {
        Todos,
        AddTodo
    }
};
</script>
