<template>
    <h2 class="title">Classement</h2>
    <router-link :to="'/equipes/' + team.idTeam" v-for="team in list" :key="team.intRank" style="border-bottom:1px solid grey;">
    <ion-card style="background-color: #0768ba;">
      <ion-card-content>
            <ion-grid>
              <ion-row>
                <ion-col>
                  <ion-label style="color: white; margin-bottom: 20px; display: block;">{{ team.intRank }} - {{ team.strTeam }}</ion-label>
                  <img :alt="team.strTeam" :src="team.strTeamBadge" />
                </ion-col>
                <ion-col>
                  <p style="color: white;">Pts : {{ team.intPoints }}</p>
                  <p style="color: white;">J : {{ team.intPlayed }} | G : {{ team.intWin }}</p>
                  <p style="color: white;">N: {{ team.intDraw }} | P : {{ team.intLoss }}</p>
                </ion-col>
              </ion-row>
            </ion-grid>
      </ion-card-content>
    </ion-card>
  </router-link>
  
</template>

<script>
    import { IonCard, IonCardContent, IonCardHeader, IonCardSubtitle, IonCardTitle, IonCol, IonGrid } from '@ionic/vue';
    import { defineComponent } from 'vue';

export default {
  data(){
    return{
      id: "",
      list: []
    }
  },
  components: { IonCard, IonCardContent, IonCardHeader, IonCardSubtitle, IonCardTitle },
  methods: {
    
    getClassement(){
      fetch(`https://www.thesportsdb.com/api/v1/json/3/lookuptable.php?l=${this.id}&s=2022-2023`)
            .then(response => response.json())
            .then(json => {
              console.log(json);

              this.list = json.table
            })
    }

  },
  mounted() {
    this.id = this.$route.params.id
    console.log(this.id);

    this.getClassement()
  },
}
</script>
<style scoped>
    ion-item {
      --padding-start: 0;
    }
  </style>