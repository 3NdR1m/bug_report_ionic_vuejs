<template>
  <ion-page>
  Data is {{ data }}.
  <br>
  It should be '5'.
  </ion-page>
</template>

<script lang="ts">
import { IonContent, IonHeader, IonPage, IonTitle, IonToolbar } from '@ionic/vue';
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'HomePage',
  data() {
    return {
      data: 0
    }
  },
  components: {
    IonPage,
  },
  beforeRouteEnter(to, from, next) {
    next(e => (e as any).data = 5);
  }
});
</script>

