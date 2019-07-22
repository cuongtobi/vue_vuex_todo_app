<template>
    <form class="form-inline mt-2 mb-2" @submit.prevent="onSubmit">
        <div class="form-group">
            <input 
                v-model="title"
                type="text" 
                class="form-control mr-2" 
                placeholder="Add todo..." />
        </div>
        <button type="submit" class="btn btn-primary">Save</button>
    </form>
</template>

<script>
import { mapActions } from 'vuex';

export default {
    name: 'AddTodo', 
    data() {
        return {
            title: ''
        }
    }, 
    methods: {
        ...mapActions(['addTodo']), 
        onSubmit() {
            this.addTodo(this.title);
        }
    }
}
</script>
