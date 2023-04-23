<template>
  <h2 class="title">{{ id }} - Equipes</h2>
 <div class="grid">
  <router-link :to="{ name: 'equipe', params: { id: team.idTeam } }" v-for="team in list" :key="team.strTeam">
    <ion-card style="background-color: #0768ba; width: 100%; height: 100%; margin-inline: 0px;">
      <ion-card-content>
        <ion-label style="color: white; margin-bottom: 20px; display: block;">{{ team.strTeam }} - {{ team.strCountry }}</ion-label>
        <img :alt="team.strTeam" :src="team.strTeamLogo" style="width: 100px"/>
      </ion-card-content>
    </ion-card>
  </router-link>
 </div>

</template>


<script>
  import { IonCard, IonCardContent, IonCardHeader, IonCardSubtitle, IonCardTitle } from '@ionic/vue';
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
  
  getEquipes(){
    fetch(`https://www.thesportsdb.com/api/v1/json/3/search_all_teams.php?l=${this.id}`)
      .then(response => response.json())
      .then(json => {
        console.log(json);

        this.list = json.teams
      })
  }

},
mounted() {
  this.id = this.$route.params.id
  console.log(this.id);

  this.getEquipes()
},
}
</script>
<style scoped>
  ion-item {
    --padding-start: 0;
  }
  .grid{
    width: 100%;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
  }
</style>