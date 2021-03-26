<template>
  <div id="app">
    <HeaderTodo :HeaderLinks="HeaderLinks"/>
    <TodoList :tasks="tasks" :text="text" @delete-task="deleteTask"/>
    <h1>{{tasks}}</h1>
  </div>
</template>


<script>
  import HeaderTodo from "./components/HeaderTodo";
  import TodoList from "./components/TodoList";
export default {
  name: 'app',
  data(){
    return{
      HeaderLinks: ['<a href="">Google</a>', '<a href="">Yandex</a>', '<a href="">MailRu</a>', '<a href="">Bingo</a>'],
      text: 'Hello World!',
      tasks: ['Ремонт', 'Завтрак', 'Lololoshka', 'VanTuz', 'Чета еще'],
    }
  },
  components: {
    HeaderTodo,
    TodoList
  },
  methods: {
    deleteTask(index){
      this.tasks.splice(index, 1)
    }
  }
}
</script>












<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
  .todo__wrapper{
    border: 4px solid #30c5ff;
    ul, li{
      text-decoration: none;
    }
    .todo__body{
      width:450px;
      border: 1px solid red;
      margin: auto;
    }
  }
</style>
