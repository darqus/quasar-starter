<template>
  <q-toggle
    v-model="isThemeDark"
    size="xl"
    :icon="isThemeDark ? 'dark_mode' : 'light_mode'"
    :label="isThemeDark ? 'dark' : 'light'"
    @click="toggleTheme"
  />
</template>

<script setup lang="ts">
import { ref } from 'vue'
import { useQuasar } from 'quasar'

const $q = useQuasar()
const isThemeDark = ref(true)

const toggleTheme = () => {
  $q.dark.toggle()
}
</script>
