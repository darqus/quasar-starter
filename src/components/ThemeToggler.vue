<template>
  <q-toggle
    v-model="isThemeDark"
    @click="toggleLeftDrawer"
    label="Toggle Theme"
  />
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue'
import { useQuasar } from 'quasar'

export default defineComponent({
  name: 'ThemeToggler',

  setup() {
    const $q = useQuasar()
    const isThemeDark = ref(true)

    return {
      isThemeDark,
      toggleLeftDrawer() {
        $q.dark.toggle()
      }
    }
  }
})
</script>
