<template>
  <div>
    <v-row>
      <v-col cols="12" xs="12">
        <CategoriaList/>
      </v-col>
    </v-row>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator'
import { RequiresAuth, RequiredAccess } from '~/middleware'

@Component({
  meta: {
    auth: {
      requiredAccess: true,
      requiresAuth: true
    },
  },
  middleware: [RequiresAuth, RequiredAccess]
})
export default class CategoriaListPage extends Vue {
  
}
</script>

<style>
</style>