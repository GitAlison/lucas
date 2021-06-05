<template>
  <ion-page>
    <ion-content>
      <div class="container-login">
        <h1 class="ion-no-margin">Olá</h1>
        <p class="ion-no-margin">Está pronto pra mudar sua vida?</p>
        <div class="divider-h"></div>

        <form action="" method="post">
          <label for="login">Seu Login</label>
          <input
            id="login"
            class="input-control"
            placeholder="contato@teste.com.br"
            type="text"
          />

          <label for="password">Senha</label>
          <input
            id="password"
            class="input-control"
            placeholder="**************"
            type="password"
          />
          <div class="divider-h"></div>
          <ion-button
            @click="() => router.push('/tabs')"
            color="primary"
            expand="block"
            mode="ios"
            >Fazer Login</ion-button
          >
        </form>
      </div>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { IonContent } from "@ionic/vue";
import { useRouter } from "vue-router";

export default {
  name: "Tab2",
  components: {
    IonContent,
  },
  setup() {
    const router = useRouter();
    return { router };
  },
};
</script>

<style >
.container-login {
  padding: 70px 30px 30px 30px;
}
</style>