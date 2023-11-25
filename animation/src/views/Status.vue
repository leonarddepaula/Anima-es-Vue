<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <div>
        <div v-if="!pokemon.status">
            <h2 class="text-center">Selecione um Pokémon</h2> 
         </div>
         <div v-else>
        <span>Força:</span>
        <div class="progress mb-2">
            <div 
                class="progress-bar" 
                role="progressbar" 
                :style="`width: ${pokemon.status.forca}%`"
                :aria-valuenow="pokemon.status.forca" 
                aria-valuemin="0" 
                aria-valuemax="100"
                >
                {{pokemon.status.forca}}
            </div>
        </div>

        <span>Agilidade:</span>
        <div class="progress mb-2">
            <div class="progress-bar" role="progressbar" :style="`width: ${pokemon.status.agilidade}%`"
                :aria-valuenow="pokemon.status.agilidade" aria-valuemin="0" aria-valuemax="100">40</div>
        </div>

        <span>Ataque:</span>
        <div class="progress mb-2">
            <div class="progress-bar" role="progressbar" :style="`width: ${pokemon.status.ataque}%`"
                :aria-valuenow="pokemon.status.ataque" aria-valuemin="0" aria-valuemax="100">20</div>
        </div>

        <span>Defesa:</span>
        <div class="progress mb-2">
            <div class="progress-bar" role="progressbar" :style="`width: ${pokemon.status.defesa}%`"
                :aria-valuenow="pokemon.status.defesa" aria-valuemin="0" aria-valuemax="100">25</div>
        </div>
        </div>
    </div>
</template>

<script>
export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: 'Status',
    props: {
        pokemon: Object
    }
}
</script> 