<template>
  <div id ="app">
    <Todos />
    </div>
</template>

<script>
import Todos from './components/Todos';

export default {
  name: 'app',
  components: {
    Todos
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
}
</script>

<style>

</style>
