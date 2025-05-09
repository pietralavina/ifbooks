<script setup>
  import { ref } from 'vue';

  const exibeCarrinho = false;

  const professor = ref({
    nome: 'Eduardo da Silva',
    disciplinas: [
      'Desenvolvimento Web II',
      'Desenvolvimento de Aplicativos para Dispositivos Móveis',
    ],
  });

  function mostraCarrinho() {
    exibeCarrinho = !exibeCarrinho;
    return exibeCarrinho;
  }
</script>

<template>
  <div>
    <h1>Professor</h1>
    <p>Nome: {{ professor.nome }}</p>
    <p v-if="!exibeCarrinho">Carrinho oculto.</p>
    <div v-else>
      <p>Carrinho de Compra.</p>
      <ul>
        <li v-for="disciplina in professor.disciplinas" :key="disciplina">
          {{ disciplina }}
        </li>
      </ul>
    </div>
  </div>
</template>
<style scoped></style>