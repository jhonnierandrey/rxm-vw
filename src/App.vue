<template>
  <div class="container">
    <div class="logo-container">
      <a href="https://rickandmortyapi.com/" target="_blank" title="Visit API"><img src="rxm_logo.svg" alt="Rick And Morty" srcset=""></a>
    </div>
    <FilterByStatus />
    <FilterByName />
    <ListCharacters />
    <Footer />
  </div>
</template>

<script>
import ListCharacters from '@/components/ListCharacters'
import FilterByStatus from '@/components/FilterByStatus'
import FilterByName from '@/components/FilterByName'
import Footer from '@/components/Footer'

export default {
  title: 'Rick And Morty with Vue',
  name: 'App',
  components: {
    ListCharacters,
    FilterByStatus,
    FilterByName,
    Footer
  },
}
</script>

<style lang="scss">
:root{
  // --background-body: #24282F;
  --background-body: #181c2b;
  --background-card: rgba(60, 62, 68, 0.5);
  --text-white: #FFFFFF;
  --text-gray : #C0C0C0;
  --text-orange: #FF9800;
  --border-yellow: #BFDE42;
}

* {
  box-sizing : border-box;
  margin : 0;
  padding: 0;
}

body {
  background-image: url('/background.png');
  background-color: var(--background-body);
  background-blend-mode: hard-light;
  background-size: cover;
  color: var(--text-white);
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

h1 {
  margin-bottom: 3rem;
  text-align: center;
}

.container {
  width: 980px;
  max-width: 90%;
  margin: 3rem auto;

  .logo-container {
    text-align: center;
    
    img {
      padding-bottom: 1rem;
      width: 50%;

      &:hover {
        transform: scale(1.1);
        transition: transform 200ms ease-in-out;
      }
    }
  }
}

img {
  width: 100%;
}
</style>
