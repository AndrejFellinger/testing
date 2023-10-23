<template>
	<!-- 1. Moveni si toto do novej page, ktoru sprav napr v src/plugins/app@feed/feed.vue -->
	<!-- 2. Fixni si router, lebo po prekliku z tabov sa to nezobrazi -->
	<!-- 3. Presun component do src/plugins/app@feed/_components/a-featured-posts-slider.vue -->
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