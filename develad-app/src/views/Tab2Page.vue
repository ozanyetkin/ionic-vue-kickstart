<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Tab 1</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Tab 1</ion-title>
        </ion-toolbar>
      </ion-header>

      <ExploreContainer name="Tab 2 page" />

      <iframe src="https://webar.imaginerealities.com.au/wt/demo/" width="100%"
        height="800px"></iframe>
    </ion-content>
  </ion-page>
</template>

<script setup lang="ts">
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent } from '@ionic/vue';
import { ref, onMounted } from 'vue';
import { Motion } from '@capacitor/motion';

const hasPermission = ref(false);

onMounted(async () => {
  try {
    await DeviceMotionEvent.requestPermission();
    hasPermission.value = true;
    Motion.addListener('accel', event => {
      console.log('Device motion event:', event);
    });
  } catch (error) {
    console.error('Motion permission not granted:', error);
  }
});
</script>