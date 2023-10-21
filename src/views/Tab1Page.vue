<template>
  <Hero :data="hero" />
</template>

<script setup>
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent } from '@ionic/vue';
import Hero from '@/components/HeroComp.vue';


</script>

<script>
  export default{
  data() {
    return {
      hero: [
        {
          url: "https://tinyhousetalk.com/wp-content/uploads/400-sq-ft-cabin-by-wheelhaus-the-wedge-00011.jpg",
          badgeTitle: "Článok",
          title: "Inovatívny startup prináša cenovo dostupné montované chatky",
          hashtags: ["inovacie", "biznis", "startupy", "fyp"]
        }
      ],
    }
  },
}
</script>