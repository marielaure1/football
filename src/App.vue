<template>
  <ion-menu content-id="main-content">
    <ion-content class="ion-padding" id="menu-content"> 
      <router-link to="/ligues/4334/classement" router-direction="forward" >Classement Ligue 1</router-link>
      <router-link to="/ligues/French Ligue 1/equipes" router-direction="forward" >Equipes Ligue 1</router-link>

      <router-link to="/ligues/4401/classement" router-direction="forward" >Classement Ligue 2</router-link>
      <router-link to="/ligues/French Ligue 1/equipes" router-direction="forward" >Equipes Ligue 2</router-link>

      <router-link to="/ligues/4504/classement" router-direction="forward" >Classement Coupe de France</router-link>
      <router-link to="/ligues/Coupe de France/equipes" router-direction="forward" >Equipes Coupe de France</router-link>

      <router-link to="/ligues/4480/classement" router-direction="forward" >Classement Champion's league </router-link>
      <router-link to="/ligues/Champion's League/equipes" router-direction="forward" >Equipes Champion's league </router-link>
    </ion-content>
  </ion-menu>

  <ion-page id="main-content">
    <ion-header>
      <ion-toolbar>
        <ion-buttons slot="start">
          <ion-menu-button style="color: white;"></ion-menu-button>
        </ion-buttons>
        <ion-title>Ionic Football</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content class="ion-padding">
        <router-view></router-view>
        
     
    </ion-content>
  </ion-page>

</template>

<script>
  import {
    IonButtons,
    IonContent,
    IonHeader,
    IonMenu,
    IonMenuButton,
    IonPage,
    IonTitle,
    IonToolbar,
    IonRouterOutlet 
  } from '@ionic/vue';
  import { defineComponent } from 'vue';

  export default defineComponent({
    components: {
      IonButtons,
      IonContent,
      IonHeader,
      IonMenu,
      IonMenuButton,
      IonPage,
      IonTitle,
      IonToolbar, 
      IonRouterOutlet
    },
  });
</script>

<style>
ion-header{
  padding: 20px;
}

ion-toolbar{
  height: 100%;
  background-color: transparent;
}

.header-md::after{
  display: none;
}

:root{
  font-family: 'Raleway', sans-serif;
}

ion-title{
  text-align: center;
  font-weight: 700;
  font-size: 32px;
  color: white;
}

#main-content ion-header{
  background: linear-gradient(#053d79, #044484);
}

.md.content-ltr, #background-content{
  background-color: transparent!important;
}

#menu-content{
  background: linear-gradient(#053d79, #044484);
  display: flex;
  flex-direction: column;
}

#menu-content a:first-child{
  margin-top: 60px;
}

#menu-content a{
  color: white;
  display: block;
  margin-bottom: 10px;
  font-size: 18px;
}

:root{
  --ion-background-color: transparent;
}

.title{
  margin-bottom: 40px; 
  color: white; 
  font-weight: 600;
}

a{
  text-decoration: none;
}

.button-inner{
  color: white!important;
}
</style>