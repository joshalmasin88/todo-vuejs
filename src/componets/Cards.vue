<template>
  <div>
    {{ nameText }}
    <div class="text-center">
      <input type="text" v-model="todo" class="form-control" placeholder="Add To Do..">
      <button class="btn btn-primary mt-2 mb-2" @click="addTodo">Add Todo</button>
    </div>
    <div class="card" v-for="(item,index) in todoList" :key="index">
      <p class="card-title text-right p-2 text-danger" @click="removeTodo(index)"><strong>X</strong></p>
      <h4 class="card-title text-center mt-2">{{ index }}</h4>
      <p class="card-text p-4 text-center">
        {{ item }}
      </p>
    </div>
  </div>
</template>

<script>

export default {
  props: ['nameText '],
  data() {
    return {
      todo: '',
      todoList: []
    }
  },
  methods: {
    addTodo() {
      this.todoList.push(this.todo)
      this.todo = ""
    },
    removeTodo(index) {
      console.log(index)
      this.todoList.splice(index,1)
      this.todo = ""
    }
  }
};
</script>

