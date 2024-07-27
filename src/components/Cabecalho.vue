<script setup>
import { defineProps } from 'vue';

const props = defineProps(['tarefasPendentes']);
</script>

<template>
  <header class="p-5 mb-4 mt-4 bg-light rounded-3">
    <h1>Minhas Tarefas</h1>
    <p>
      Você possui {{ tarefasPendentes }} tarefas pendentes
    </p>
  </header>
</template>

<style scoped>
.header {
  background-color: #f5f5f5;
  padding: 10px;
  text-align: center;
}
</style>
