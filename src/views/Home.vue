<template>
  
  <ion-card style="background-color: #0768ba;" class="ion-padding">
    <ion-grid>
      <ion-row>
        <ion-col>
            <ion-card-title class="title">Ligue 1</ion-card-title>
          
            <router-link to="/ligues/4334/classement" style="margin-bottom: 10px; display: block; color: white;"><ion-icon name="arrow-forward-outline"></ion-icon> Voir le classement</router-link>
            <router-link to="/ligues/French Ligue 1/equipes" style="margin-bottom: 10px; color: white;"><ion-icon name="arrow-forward-outline"></ion-icon> Voir les équipes</router-link>
        </ion-col>
        <ion-col>
          <ion-card-content style="display: flex; justify-content: end;">
            <img alt="Silhouette of mountains" src="/ligue1.png" style="width: 70px; "/> 
          </ion-card-content>
        </ion-col>
      </ion-row>
    </ion-grid>
  </ion-card>

  <ion-card style="background-color: #0768ba;" class="ion-padding">
    <ion-grid>
      <ion-row>
        <ion-col>
            <ion-card-title class="title">Ligue 2</ion-card-title>
          
            <router-link to="/ligues/4401/classement" style="margin-bottom: 10px; display: block; color: white;"><ion-icon name="arrow-forward-outline"></ion-icon> Voir le classement</router-link>
            <router-link to="/ligues/French Ligue 1/equipes" style="margin-bottom: 10px; color: white;"><ion-icon name="arrow-forward-outline"></ion-icon> Voir les équipes</router-link>
        </ion-col>
        <ion-col>
          <ion-card-content style="display: flex; justify-content: end;">
            <img alt="Silhouette of mountains" src="/ligue2.png" style="width: 70px; "/> 
          </ion-card-content>
        </ion-col>
      </ion-row>
    </ion-grid>
  </ion-card>

  <ion-card style="background-color: #0768ba;" class="ion-padding">
    <ion-grid>
      <ion-row>
        <ion-col>
            <ion-card-title class="title">Coupe de France</ion-card-title>
          
            <router-link to="/ligues/4504/classement" style="margin-bottom: 10px; display: block; color: white;"><ion-icon name="arrow-forward-outline"></ion-icon> Voir le classement</router-link>
            <router-link to="/ligues/Coupe de France/equipes" style="margin-bottom: 10px; color: white;"><ion-icon name="arrow-forward-outline"></ion-icon> Voir les équipes</router-link>
        </ion-col>
        <ion-col>
          <ion-card-content style="display: flex; justify-content: end;">
            <img alt="Silhouette of mountains" src="/coupedefrance.jpeg" style="width: 70px; "/> 
          </ion-card-content>
        </ion-col>
      </ion-row>
    </ion-grid>
  </ion-card>

  <ion-card style="background-color: #0768ba;" class="ion-padding">
    <ion-grid>
      <ion-row>
        <ion-col>
            <ion-card-title class="title">Champion's League</ion-card-title>
          
            <router-link to="/ligues/4480/classement" style="margin-bottom: 10px; display: block; color: white;"><ion-icon name="arrow-forward-outline"></ion-icon> Voir le classement</router-link>
            <router-link to="/ligues/Champion's League/equipes" style="margin-bottom: 10px; color: white;"><ion-icon name="arrow-forward-outline"></ion-icon> Voir les équipes</router-link>
        </ion-col>
        <ion-col>
          <ion-card-content style="display: flex; justify-content: end;">
            <img alt="Silhouette of mountains" src="/championsleague.jpg" style="width: 70px; "/> 
          </ion-card-content>
        </ion-col>
      </ion-row>
    </ion-grid>
  </ion-card>
</template>

<script setup>
import { IonContent, IonHeader, IonPage, IonTitle, IonToolbar, IonApp, IonRouterOutlet, IonSelect, IonSelectOption, IonItem, IonList, IonCardTitle, IonCardHeader, IonCardContent, IonCard, IonButton  } from '@ionic/vue';
import { DateTime } from "luxon";

</script>

<script>

export default {
  data(){
    return{
    }
  },
  components: { IonContent, IonHeader, IonPage, IonTitle, IonToolbar, IonApp, IonRouterOutlet, IonSelect, IonSelectOption, IonItem, IonList, IonCardTitle, IonCardHeader, IonCardContent, IonCard, IonButton  },
  methods: {
  }
}
</script>
