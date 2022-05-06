<template>
  <TodoList />
</template>

<script>
  import TodoList from './components/TodoList.vue'

  export default {
    name: 'App',
    components: {
      TodoList
    }
  }
</script>

<style>
  * {
    margin: 0;
    padding: 0;
  }
  .container{
      display: flex;
      flex-direction: column;
      justify-content: center;
      background-color: #808080;
      color: #fff;
      min-height: 100vh;
    }

    .entrada {
      width: 25%;
      margin: 20px auto;
      padding: 10px;
    }

    .lista{
      width: 25%;
      margin: 20px auto;
      background-color: #000;
    }

    .lista button {
      width: 20px;
      float: right;
    }

    ul li {
      list-style-type: none;
      text-align: center;
      margin-bottom: 10px;
      padding: 10px;
    } 

    #inserir {
      width: 70px;
      padding: 10px;
      margin: 0 auto;
      cursor: pointer;
    }
</style>
