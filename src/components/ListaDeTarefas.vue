<script setup>
const props = defineProps(['tarefas']);
</script>

<template>
  <ul v-if="tarefas.length > 0" class="list-group mt-4">
    <li class="list-group-item" v-for="tarefa in tarefas" :key="tarefa.titulo">
      <input @change="evento => tarefa.finalizada = evento.target.checked" :checked="tarefa.finalizada" :id="tarefa.titulo" type="checkbox">
      <label :class="{ done: tarefa.finalizada }" class="ms-3" :for="tarefa.titulo">
        {{ tarefa.titulo }}
      </label>
    </li>
  </ul>
  <span v-else>Ahazou, fez tudo!</span>
</template>

<style scoped>
.done {
  text-decoration: line-through;
}
</style>
