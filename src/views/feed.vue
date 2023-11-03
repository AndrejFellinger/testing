<template>
  <FeaturedPostSlider :data="post" />
</template>

<script setup>
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent } from '@ionic/vue';
import FeaturedPostSlider from '../plugins/app@feed/_components/a-featured-posts-slider.vue';


</script>

<script>
  export default{
  data() {
    return {
      post: [
        {
          url: "https://tinyhousetalk.com/wp-content/uploads/400-sq-ft-cabin-by-wheelhaus-the-wedge-00011.jpg",
          badgeTitle: "Článok",
          title: "Inovatívny startup prináša cenovo dostupné montované chatky.",
          hashtags: ["inovacie", "biznis", "startupy", "fyp"],
        },
        {
          url: "https://m.media-amazon.com/images/M/MV5BZjJiZTBiNDktNzk4OS00NmFiLWIyZTMtYzdhMWJhZGJkYmU3XkEyXkFqcGdeQXVyMjIxMzMyMQ@@._V1_.jpg",
          badgeTitle: "Článok",
          title: "Markíza stratila čaro klasických Vianoc. Pelíšky už si na Markíze nepozriete.",
          hashtags: ["vianoce", "markiza", "novinky", "fyp"],
        },
        {
          url: "https://a57.foxnews.com/static.foxnews.com/foxnews.com/content/uploads/2023/10/1200/675/Israeli-airstrike-in-Gaza.jpg?ve=1&tl=1",
          badgeTitle: "Článok",
          title: "Siruácia v Gaze sa stále zhoršuje. Od vypuknutia vojny bol zaznamenaný rekordný počet obetí.",
          hashtags: ["vojnavizraeli", "izrael", "novinky", "fyp"],
        }
      ],
    }
  },
}

</script>