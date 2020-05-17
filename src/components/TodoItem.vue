<template>
  <div class="todo-item" v-bind:class="{'is-complete':todo.completed}">
    <p>
      <input type="checkbox" v-on:change="markComplete" />
      {{todo.title}}
      <button @click="$emit('del-todo', todo.id)" class="del">x</button>
    </p>
  </div>
</template>

<script>
export default {
  name: "TodoItem",
  props: ["todo"],
  methods: {
    markComplete() {
      this.todo.completed = !this.todo.completed;
    }
  }
};
</script>

<style scoped>
.todo-item {
  padding: 10px;
  background: #f4f4f4;
  border-bottom: 1px dotted #ccc;
}

.is-complete {
  text-decoration: line-through;
}

.del {
  float: right;
  padding: 5px 10px;
  color: #fff;
  background: #ff0000;
  border: none;
  border-radius: 50%;
  cursor: pointer;
}
</style>