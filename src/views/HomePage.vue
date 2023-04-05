<template>
  <ion-page>
    <ion-content :fullscreen="true">
      <ion-grid style="max-width: 500px;">
        <ion-row>
          <ion-col style="padding: 20px;">
            <ion-input aria-label="" class="custom-input" fill="outline"></ion-input> 
          </ion-col>
        </ion-row>
        <ion-row>
          <ion-col style="padding: 20px;">
            <ion-select class="custom-select" aria-label="" fill="outline">
              <ion-select-option v-for="[value, text] in choices" :value="value" :key="value">{{ text }}</ion-select-option>
            </ion-select> 
          </ion-col>
        </ion-row>
        <ion-row>
          <ion-col style="padding: 20px;">
            <ion-textarea class="custom-textarea" aria-label="" fill="outline"></ion-textarea> 
          </ion-col>
        </ion-row>
      </ion-grid>
    </ion-content>
  </ion-page>
</template>

<script setup lang="ts">
import { IonPage, IonContent, IonInput, IonGrid, IonRow, IonCol, IonSelect, IonSelectOption, IonTextarea } from '@ionic/vue';

const choices = new Map([
  ['1', 'Choice 1'],
  ['2', 'Choice 2'],
  ['3', 'Choice 3'],
  ['4', 'Choice 4'],
]);

</script>

<style scoped>
  ion-input.custom-input{
    --border-radius: 30px; /* does not apply to top left and bottom left corners */
    --border-width: 2px;
  }

  ion-select.custom-select{
    --border-radius: 30px; /* does not apply to top left and bottom left corners */
    --border-width: 2px;
  }

  ion-textarea.custom-textarea{
    --border-radius: 30px; /* does not apply to top left and bottom left corners */
    --border-width: 2px;
  }

</style>
