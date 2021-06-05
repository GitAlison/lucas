<template>
  <ion-card class="ion-no-margin">
    <ion-card-header>
      <ion-card-title @click="() => router.push('/notice-detail')"
        >unt aut facere repellat provident occaecati excepturi optio
        reprehenderit</ion-card-title
      >
    </ion-card-header>

    <ion-card-content>
      <div @click="() => router.push('/notice-detail')">
        quia et suscipit\nsuscipit recusandae consequuntur expedita et
        umnreprehenderit molestiae ut ut quas totam\nnostrum rerum est autem
        sunt rem eveniet architecto
      </div>
      <div class="card-actions">
        <div class="ion-activatable action-button ripple" @click="toggle()">
          <ion-icon :style="{ color: selected ? 'red' : '' }" :icon="heart" />
          <span>{{ likes }}</span>
          <ion-ripple-effect type="unbounded"></ion-ripple-effect>
        </div>

        <div class="ion-activatable action-button ripple">
          <ion-icon :icon="chatbubbleEllipses" />
          <span>248</span>
          <ion-ripple-effect type="unbounded"></ion-ripple-effect>
        </div>
      </div>
    </ion-card-content>
  </ion-card>
</template>

<script>
import {
  IonCard,
  IonCardContent,
  IonCardHeader,
  IonCardTitle,
  IonRippleEffect,
} from "@ionic/vue";
import { heart, chatbubbleEllipses } from "ionicons/icons";
import { useRouter } from "vue-router";
export default {
  name: "CardNotice",
  components: {
    IonCard,
    IonCardContent,
    IonCardHeader,
    IonCardTitle,
    IonRippleEffect,
  },
  data: () => ({
    selected: false,
    likes: 1125,
  }),
  setup() {
    const router = useRouter();
    return {
      heart,
      chatbubbleEllipses,
      router,
    };
  },
  methods: {
    toggle() {
      this.selected = !this.selected;
      if (this.selected) {
        this.likes++;
      } else {
        this.likes--;
      }
    },
  },
};
</script>

<style scoped>
.ripple {
  position: relative;
  overflow: hidden;
}
.card-actions {
  margin-top: 27px;
  margin-bottom: 10px;
  display: flex;
  gap: 17px;
}
.card-actions .action-button {
  display: flex;
  align-items: center;
  border-radius: 10px;
  padding: 0 2px;
}
.card-actions ion-icon {
  color: #b5bbc6;
  font-size: 22px;
  margin-right: 3px;
}
.card-actions ion-icon .active {
  color: #f92d56 !important;
}
.card-actions span {
  color: #000;
  font-size: 15px;
}
</style>