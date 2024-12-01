<template>
  <div>
    <h1>Personajes de mi lista</h1>
    <CharactersList :characters="characters" />
  </div>
</template>
<script lang="ts" setup>
import { useCharacterStore } from '@/stores/useCharacterStore'
import { computed } from 'vue'
import CharactersList from './CharactersList/CharactersList.vue'

console.log('Characters')
const characterStore = useCharacterStore()

const characters = computed(() => characterStore.formattedCharacters)
// TODO: aca tenemos que traer los datos de los personajes
</script>
<style lang="scss"></style>
