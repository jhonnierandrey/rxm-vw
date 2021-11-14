<template>
  <footer id="footer">
        <ul className="footer-copyright">
            <li>&copy; 2021 <a href="https://www.jaesmadeit.com/" target="_blank" rel="noopener noreferrer">JAES Made It</a></li>
            <li>Made with <a href="https://vuejs.org/" target="_blank" rel="noopener noreferrer">Vue</a> + <a href="https://rickandmortyapi.com/" target="_blank" rel="noopener noreferrer"> RickAndMorty API </a> + <a href="https://github.com/jhonnierandrey/rxm-vw" target="_blank" rel="noopener noreferrer">GitHub</a></li>
            <li><a href="http://jhonnierandrey.info/" target="_blank" rel="noopener noreferrer">See more</a></li>
            <li><a href="https://www.buymeacoffee.com/jhonnierandrey" target="_blank" rel="noopener noreferrer"><i className="fas fa-coffee"></i></a></li>
        </ul>
  </footer>
</template>

<script>
export default {

}
</script>

<style lang="scss">
#footer {
    text-align: center;
    a {
        text-decoration: none;
        color: var(--text-orange);

        &:hover {
            color: var(--border-yellow);
        }
    }
    ul {
        list-style: none;
    }
}

</style>