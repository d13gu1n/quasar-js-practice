<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-toolbar-title> Ambiente de Quasar </q-toolbar-title>

        <div>Quasar v{{ $q.version }}</div>
      </q-toolbar>
    </q-header>
    <q-page-container>
      <q-btn unelevated dense label="Probá" no-caps color="primary" @click="testMethod" class="q-py-sm" />
      <JSJamboard :passedTestLabel="testLabel"/>
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue'
import JSJamboard from 'components/JSJamboard.vue'
let testLabel

export default defineComponent({
  name: 'MainLayout',

  components: {
    JSJamboard,
  },
  data() {
    return {
      ref,
      testLabel,
    }
  },

  methods: {
    // TODO: Practice methods and algorithms here
    testMethod() {
      console.log('It works!! 💓')
      this.testLabel = 'It is, indeed, working!! 💓'
    },
  },
})
</script>
