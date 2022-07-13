<template>
  <q-page class="flex flex-center bg-primary">
    <q-card style="width: 300px; height: auto; display: flex; flex-direction: column; align-items: center">

      <img src="../assets/logo.png" ratio="1" style="width: 200px"/>

      <q-card-section>
        <div class="text-h5 q-pt-none">Aprendendo-QUASAR</div>
      </q-card-section>

      <q-card-section class="q-pt-none full-width">
        <q-input filled v-model="login.email" label="Email" />
        <q-input class="q-mt-sm" v-model="login.password" filled :type="login.isPwd ? 'password' : 'text'" label="Senha">
          <template v-slot:append>
            <q-icon
              :name="login.isPwd ? 'visibility_off' : 'visibility'"
              class="cursor-pointer"
              @click="login.isPwd = !login.isPwd"
            />
          </template>
        </q-input>
      </q-card-section>

      <q-card-actions class="full-width">
        <q-btn @click="$router.push({ name: 'home' })" class="q-mx-sm" style="width: 100%" outline color="primary" label="Login" />
      </q-card-actions>

      <q-card-actions class="full-width">
        <q-btn @click="$router.push({ name: 'esqueciSenha' })" flat no-caps class="q-mx-sm" style="width: 100%" outline color="primary" label="Esqueci minha senha" />
      </q-card-actions>

    </q-card>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'LoginPage',
  data () {
    return {
      login: {
        email: '',
        password: '',
        isPwd: true
      }
    }
  }
})
</script>
