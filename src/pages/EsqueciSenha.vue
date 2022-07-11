<template>
  <q-page class="flex flex-center bg-primary">
    <q-card style="width: 300px; height: auto; display: flex; flex-direction: column; align-items: center">

      <q-card-section class="full-width">
        <div class="text-h5">Esqueci minha senha</div>
        <div class="text-subtitle">Informe seu email para recuperar a senha</div>
      </q-card-section>

      <q-card-section class="q-pt-none full-width q-mt-sm">
        <q-input filled v-model="email" label="Email" />
      </q-card-section>

      <q-card-actions class="full-width">
        <q-btn @click="$router.push({ name: 'login' })" class="q-mx-sm" style="width: 100%" outline color="primary" label="Redefinir Senha" />
      </q-card-actions>

    </q-card>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'EsqueciSenha',
  data () {
    return {
      email: ''
    }
  }
})
</script>
