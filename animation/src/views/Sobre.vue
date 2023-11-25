<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <div>
        <div v-if="!pokemon.id">
           <h2 class="text-center">Selecione um Pokémon</h2> 
        </div>
        <div v-else>
            <p>Identificador: {{ pokemon.id }}</p>
            <p>Nome: {{ pokemon.nome }}</p>
            <p>Tipo: {{ pokemon.tipo }}</p>
        </div>

    </div>
</template>

<script>
export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: 'Sobre',
    props: {
        pokemon: Object
    }
}
</script> 