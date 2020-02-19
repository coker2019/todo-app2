<template>
    <div class="container">
        <input type="text" class="todo-input" placeholder="ENTER LIST" v-model="todo">
        <button type="submit" @click="AddTodo">ADD</button>
        <button type="submit" @click="updateTodo">update</button>
        <div v-for="(item, index) in todos" :key="index">
            <p>
                {{item}} 
                <button type="submit" @click="deleteTodo(index)">delete</button>
                <button type="submit" @click="editTodo(index)">edit</button>
                
            </p>
        </div>

    </div>
</template>
<script>
export default {
        data(){
            return {
                todos:[],
                todo:null,
                index: null
                    
            }
        },
    
    methods:{
        AddTodo: function(){
            this.todos.push(this.todo)
            this.todo = null
        },
        deleteTodo(i){
            this.todos.splice(i, 1)
        },
        editTodo(i){
            this.todo = this.todos[i]
            this.index = i
        },
        updateTodo(){
            this.todos[this.index] = this.todo
            this.todo = null
        }
    }
}
</script>
<style>
 .todo-input {
     width:50%;
     padding: 10px 18px;
     font-size:20px;
     margin-bottom: 20px;
 }
</style>

