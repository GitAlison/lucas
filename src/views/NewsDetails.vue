<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-buttons slot="start">
          <ion-button @click="() => router.push('/tabs')">
            <ion-icon slot="icon-only" :icon="chevronBackOutline"></ion-icon>
          </ion-button>
        </ion-buttons>
        <ion-title size="small" class="ion-text-center title"
          >Notícias</ion-title
        >
        <ion-buttons slot="end">
          <ion-button>
            <ion-icon slot="icon-only" :icon="ellipsisVertical"></ion-icon>
          </ion-button>
        </ion-buttons>
      </ion-toolbar>
    </ion-header>
    <ion-content fullscreen="true">
      <div class="container-sm">
        <h1>
          Unt aut facere repellat provident occaecati excepturi optio
          reprehenderit
        </h1>
        <p>
          quia et suscipit\nsuscipit recusandae consequuntur expedita et
          umnreprehenderit molestiae ut ut quas totam\nnostrum rerum est autem
          sunt rem eveniet architecto
        </p>
        <div class="divider-h"></div>
        <h3><b>Comentários(3)</b></h3>

        <CommentNews />
        <CommentNews />
        <CommentNews />
      </div>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { IonContent } from "@ionic/vue";
import { useRouter } from "vue-router";
import {
  IonButtons,
  IonTitle,
  IonButton,
  IonHeader,
  IonToolbar,
  IonPage,
} from "@ionic/vue";
import { chevronBackOutline, ellipsisVertical } from "ionicons/icons";
import CommentNews from "@/components/CommentNews.vue";
export default {
  name: "Tab2",
  components: {
    IonContent,
    IonButtons,
    IonTitle,
    IonButton,
    IonHeader,
    IonToolbar,
    IonPage,
    CommentNews,
  },
  setup() {
    const router = useRouter();
    return { chevronBackOutline, ellipsisVertical, router };
  },
};
</script>

<style scoped >
p {
  line-height: 25px;
}
.title {
  font-family: "SF Pro Text Semibold";
  font-size: 15px;
}
</style>