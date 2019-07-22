<template>
    <div>
        <table class="table">
            <thead>
                <tr>
                    <th>#</th>
                    <th>Title</th>
                    <th></th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="todo in allTodos" :key="todo.id">
                    <td>{{ todo.id }}</td>
                    <td>{{ todo.title }}</td>
                    <td></td>
                </tr>
            </tbody>
        </table>
    </div>
</template>

<script>
import { mapGetters, mapActions } from 'vuex';

export default {
    name: 'Todos',
    methods: {
        ...mapActions(['fetchTodos'])
    },
    computed: mapGetters(['allTodos']),  
    created() {
        this.fetchTodos();
    }
}
</script>
