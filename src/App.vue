<template>
  <div id ="app">
     <Todos v-bind:todos="todos" v-on:delete-todo="deleteTodo" />
     <AddTodo v-on:add-todo="addTodo" />
    </div>
</template>

<script>
import Todos from './components/Todos';
import AddTodo from './components/AddTodo';

export default {
  name: 'app',
  components: {
    Todos,
    AddTodo
  },
  data() {
    return {
      todos: [
        {
          id: 1,
          title: 'Create Todo App',
          completed: false
        },
        {
          id: 2,
          title: 'Do 10 pressups',
          completed: false
        },
        {
          id: 3,
          title: 'Cook lunch',
          completed: false
        },
        {
          id: 4,
          title: 'Do laundry',
          completed: false
        },
        {
          id: 5,
          title: 'Read book',
          completed: false
        }
      
      ],
    }
  },
  methods: {
    addTodo(newTodoObj) {
      this.todos = [...this.todos, newTodoObj];
    },
    deleteTodo(todoId) {
      this.todos = this.todos.filter(todo => todo.id !== todoId);
    }
  }
}
</script>

<style>

</style>
