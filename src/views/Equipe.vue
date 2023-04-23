<template>

  <h2 class="title">Evenements</h2>
  <div class="grid">
     <ion-card style="background-color: #0768ba; width: 100%; height: 100%; margin-inline: 0px;" v-for="event in events" :key="event.dateEvent">
       <ion-card-content>
        <ion-grid>
          <ion-row>
            <ion-col>
              <ion-label style="color: white; margin-bottom: 20px; display: block;">{{ event.dateEvent }} {{ event.strTime }}</ion-label>
              <ion-label style="color: white; margin-bottom: 20px; display: block;">{{ event.strEvent }}</ion-label>
              <ion-label style="color: white; margin-bottom: 20px; display: block;">League : {{ event.strLeague }}</ion-label>
              <p style="color: white; margin-bottom: 20px; display: block;">{{ event.strStatus }}</p>
            </ion-col>
            <ion-col style="display: flex; justify-content: end;">
              <img :src="event.strThumb" >
            </ion-col>
          </ion-row>
         
        </ion-grid>
       </ion-card-content>
     </ion-card>
  </div>

</template>

<script>
  import { IonCard, IonCardContent, IonCardHeader, IonCardSubtitle, IonCardTitle, IonCol, IonGrid, IonLabel, IonRow } from '@ionic/vue';
  import { defineComponent } from 'vue';

export default {
data(){
  return{
    id: "",
    teamd: "", 
    events: ''
  }
},
components: { IonCard, IonCardContent, IonCardHeader, IonCardSubtitle, IonCardTitle, IonCol, IonGrid, IonLabel, IonRow  },
methods: {
  
  getEquipe(){
    // fetch(`https://www.thesportsdb.com/api/v1/json/3/lookupequipment.php?id=${this.id}`)
    //     .then(response => response.json())
    //     .then(json => {
    //       console.log(json);

    //       // this.list = json.table
    //       // https://www.thesportsdb.com/api/v1/json/3/lookupformerteams.php?id=34147178
    //       // https://www.thesportsdb.com/api/v1/json/3/eventslast.php?id={id}
    //     })


    fetch(`https://www.thesportsdb.com/api/v1/json/3/eventslast.php?id=${this.id}`)
      .then(response => response.json())
      .then(json => {
        console.log(json);

        this.events = json.results
      })

  }

},
mounted() {
  this.id = this.$route.params.id
  this.getEquipe()

 
},
}
</script>
<style scoped>
  ion-item {
    --padding-start: 0;
  }
</style>