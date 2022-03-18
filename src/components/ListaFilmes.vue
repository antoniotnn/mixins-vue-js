<template>
    <div>
        <h3>Lista Filmes</h3>
        <input type="text" placeholder="Nome do Filme" v-model="item">
        <button type="button" @click="adicionarItem()">Adicionar</button>
        <br>
        <ul>
            <li v-for="(item, index) in itens" :key="index">{{ item }}</li>
        </ul>
    </div>
</template>

<script>
import ListaMixin from '@/mixins/ListaMixin.js';

export default {
    name: 'ListaFilmes',
    mixins: [ListaMixin]
}
</script>
