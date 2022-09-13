<template>
  <ion-tab-button :key="tab.name" :tab="tab.name" :href="tab.href">
    <ion-icon :icon="tab.icon" />
    <ion-label>{{ tab.value }}</ion-label>
  </ion-tab-button>
</template>

<script>
import { IonTabButton, IonIcon, IonLabel } from '@ionic/vue'

export default {
  name: 'TabComponent',
  components: { IonTabButton, IonIcon, IonLabel },
  props: {
    tab: {
      type: Object,
      required: true,
    },
  },
}
</script>

<style scoped>

</style>