<template>
    <nav>
        <div class="container">
            <div class="logo">
                <NuxtLogo class="logo-icon" /> Carlos News
            </div>
            <ul>
                <li><nuxt-link to="/">Página Inicial</nuxt-link></li>
                <li><nuxt-link to="/sobre">Sobre</nuxt-link></li>
                <li><nuxt-link to="/contato">Contato</nuxt-link></li>
            </ul>
        </div>
    </nav>
</template>


<script lang="ts">
import Vue from 'vue'
import NuxtLogo from '~/components/NuxtLogo.vue';

export default Vue.extend({
    components: { NuxtLogo }
})


</script>
  
<style scoped>
.header {
    background-color: #333;
    color: white;
    padding: 10px 20px;
}

nav {
    background-color: #333;
    color: white;
    padding: 10px 0;
}

.container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    max-width: 1200px;
    margin: 0 auto;
}

.logo {
    display: flex;
    font-size: 1.5rem;
    font-weight: bold;
    align-items: center;
}

.logo-icon {
    margin-right: 10px;
    /* Adicione a margem desejada entre a logo e o texto */
}

ul {
    list-style-type: none;
    display: flex;
}

li {
    margin-right: 20px;
}

a {
    color: white;
    text-decoration: none;
    font-weight: bold;
}

a:hover {
    text-decoration: underline;
}
</style>
  