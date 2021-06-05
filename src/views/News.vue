<template>
  <ion-page>
    <ion-header>
      <div class="topbar">
        <ion-searchbar
          placeholder="Buscar"
          class="search-input"
          mode="ios"
        ></ion-searchbar>
        <div class="actions">
          <ion-fab-button class="button-add" size="small" color="primary"
            ><ion-icon :icon="add"
          /></ion-fab-button>
        </div>
      </div>
    </ion-header>
    <ion-content>
      <div class="container pt-0">
        <h1 class="mb-1"><b>Notícias</b></h1>
        <CardNews />
        <CardNews />
        <CardNews />
      </div>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { IonPage, IonFabButton } from "@ionic/vue";

import CardNews from "@/components/CardNews.vue";
import { add } from "ionicons/icons";

export default {
  name: "Tab1",
  components: {
    CardNews,
    IonPage,
    IonFabButton,
  },
  setup() {
    return {
      add,
    };
  },
};
</script>
<style>
.topbar {
  display: flex;
  background-color: #fff;
}
.search-input input {
  border-radius: 40px !important;
}
.actions {
  padding: 0 5px;
  padding-right: 14px;
}
</style>