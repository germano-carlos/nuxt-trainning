<!-- ~/pages/index.vue -->

<template>
  <div>
    <!-- Adicione o componente da barra de navegação -->
    <Navbar />

    <!-- Adicione o componente do perfil -->
    <ProfileCard />

    <!-- Adicione o componente de últimas notícias -->
    <LatestNews />

    <!-- Adicione o componente do rodapé -->
    <Footer />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Navbar from '~/components/Navbar.vue';
import Footer from '~/components/Footer.vue';
import ProfileCard from '~/components/ProfileCard.vue';
import LatestNews from '~/components/News.vue';

export default Vue.extend({
  name: 'IndexPage',
  components: {
    Navbar,
    Footer,
    ProfileCard,
    LatestNews,
  }
})
</script>
