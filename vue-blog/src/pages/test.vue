<template>
  <router-view />
  <q-page padding>
    <q-card>
      <q-card-section>
        text: {{ addedText }}
      </q-card-section>
      <q-card-section>
        <q-input v-model="text" />
      </q-card-section>
    </q-card>
  </q-page>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'Test',
  data () {
    return {
      text: 'abc'
    }
  },
  computed: {
    addedText (): string {
      return this.text + ' added'
    }
  }

})
</script>
