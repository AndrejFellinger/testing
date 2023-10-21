<template>
  <div>
    <div v-for="hero in $props.data" :key="hero" class="container">
      <img class="bg" :src="hero.url" alt="">
      <div class="wrap">
        <div class="top-buttons">
          <ion-icon class="icon" :icon="chevronBack" />
          <ion-icon class="icon" :icon="bookmarkOutline" />
        </div>
        <div class="bottom-container">
          <div class="badge-title">
            {{hero.badgeTitle}}
          </div>
          <h2>
            {{hero.title}}
          </h2>
          <div class="hastags">
            <div v-for="hashtags in hero.hashtags">#{{hashtags}}</div>
          </div>
          <div class="bottom">
            <div class="bottom-cont">
              <!-- tu sa data o profile budu asi getovat z databazy cize nechal som to takto natvrdo dane zatial -->
              <div class="profile">
                <div class="user-profile">
                  <img class="profile-picture" :src=profilePicture alt="">
                  <p>{{profileName}} · {{ profileSubscriberCount }}</p>
                </div>
                <!-- Aj toto co je asi match na temu (chatky) pre uzivatela co by ho mohlo zauimat - tiez sa bude vyhodnocovat niekde inde aj getovat tak som to natvrdo dal -->
                <span class="badge">{{userMatch}}%</span>
              </div>
            </div>
          </div>
        </div>
        
      </div>
    </div>
  </div>
  
</template>

<script>
import { IonTabBar, IonTabButton, IonTabs, IonLabel, IonIcon, IonicSlides, IonPage, IonRouterOutlet } from '@ionic/vue';
import { bookmarkOutline, chevronBack } from 'ionicons/icons';
 
import { defineComponent } from 'vue'

export default{
  props: {
    data: Array
  },
  data() {
    return {
      profileName: "Moderne Byvanie",
      profileSubscriberCount: "7.9k",
      profilePicture: "https://i1.sndcdn.com/avatars-000510378471-3s2an6-t500x500.jpg",
      userMatch: 97,
    }
  },
}
</script>

<style scoped>
  .bg{
    opacity: 0.35;
    border-bottom-left-radius: 15px;
    border-bottom-right-radius: 15px;
    height: 450px;
    /* width: 380px; */
    position: absolute;
    object-fit: cover;
    z-index: -1;
  }

  .container{
    height: 400px;
    /* max-width: 380px; */
  }

  .wrap{
    display: grid;
    grid-template-columns: auto;
    height: 100%;
    padding: 25px;
  }

  .bottom-container{
    display: grid;
  }

  .top-buttons{
    display: grid;
    grid-template-columns: auto auto;
    justify-content: space-between;
  }

  .top-buttons .icon{
    font-size: 32px;
  }

  .badge-title{
    text-transform: uppercase;
    background: grey;
    padding: 5px 10px;
    font-size: 12px; 
    width: fit-content;
    font-weight: bold;
    height: fit-content;
  }

  .hastags{
    font-size: 13px;
    color: rgb(234, 234, 234);
    display: flex;
    gap: 5px;
    cursor: pointer;
  }

  h2{
    margin-top: 0;
  }

  .badge{
    background: rgba(0, 128, 0, 0.8);
    padding:4px  14px;
    font-size: 14px;
    border-radius: 50px;
    font-weight: 500;
    width: fit-content;
  }

  .profile{
    display: grid;
    grid-template-columns: auto auto;
    align-items: center;
    justify-content: space-between;
  }

  .user-profile{
    display: flex;
    align-items: center;
  }

  .profile-picture{
    height: 35px;
    border-radius: 50%;
    margin-right: 8px;
  }
</style>