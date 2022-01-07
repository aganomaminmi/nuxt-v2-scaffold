<template>
  <v-row justify="center" align="center">
    <v-col cols="12" sm="8" md="6">
      <v-card>
        <v-card-title class="headline">
          Welcome to the Vuetify + Nuxt.js template
        </v-card-title>
        <v-card-text>
          <p>My name is {{ name }}.</p>
          <p>bool: {{ boolean }}</p>
        </v-card-text>
        <v-card-actions>
          <v-spacer />
          <v-btn
            color="primary"
            nuxt
            @click='toggle'
          >
            toggle
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-col>
  </v-row>
</template>

<script lang="ts">
import { defineComponent, ref } from '@nuxtjs/composition-api'

export default defineComponent({
  setup() {
    const name = ref<string>('this is name')
    const boolean = ref<boolean>(false)
    const toggle = () => {
      boolean.value = !boolean.value
    }

    return {
      name,
      boolean,
      toggle
    }
  }
})

</script>
