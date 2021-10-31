<template>
    <div style="margin: 20px">
        <ul>
            <li v-for="todo in todos">
                <input type="checkbox" v-bind:checked="todo.done" v-on:change="toggle(todo)">
                <span>{{ todo.text }}</span>
            </li>
        </ul>
        <input placeholder="タスクを追加" v-on:keyup.enter="addToDo">
    </div>
</template>

<script>
import { mapMutations } from "vuex"

export default {
    computed: {
        todos(){
          return this.$store.state.todos.list  
        } 
    },
    methods: {
        addToDo(e) {
           this.$store.commit("todos/add",e.target.value)
        },
        ...mapMutations({
            toggle: "todos/toggle"
        })
    }
    
}
</script>