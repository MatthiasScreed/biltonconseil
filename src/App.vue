<template>
  <router-view />
  <FooterSection />
</template>

<script>
import FooterSection from "./components/FooterSection.vue"; // Assurez-vous que le chemin est correct

export default {
  components: {
    FooterSection, // Enregistrez le composant Footer ici
  },
  // Autres options de composant, le cas échéant
};
</script>

<style></style>
