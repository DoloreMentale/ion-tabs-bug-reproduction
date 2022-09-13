<template>
  <ion-page>
    <ion-tabs>
      <ion-router-outlet></ion-router-outlet>

      <ion-tab-bar slot="bottom">

        <tab v-for="tab in tabs" :key="tab.name" :tab="tab" />

      </ion-tab-bar>
    </ion-tabs>
  </ion-page>
</template>

<script>
import { defineComponent } from 'vue';
import { IonTabBar, IonTabs, IonPage, IonRouterOutlet } from '@ionic/vue';
import { ellipse, square, triangle } from 'ionicons/icons';
import Tab from '@/components/Tab'

export default defineComponent({
  name: 'TabsPage',
  components: { Tab, IonTabs, IonTabBar, IonPage, IonRouterOutlet },
  setup() {
    const tabs = [
        { value: 'Tab 1', name: 'tab1', href: '/tabs/tab1', icon: ellipse },
        { value: 'Tab 2', name: 'tab2', href: '/tabs/tab2', icon: square },
        { value: 'Tab 3', name: 'tab3', href: '/tabs/tab3', icon: triangle },
    ];

    return {
      tabs,
    };
  }
});
</script>
