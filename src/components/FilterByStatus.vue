<template>
  <div class="filter">
      <div class="item" @click="filter('')">
          All
      </div>
      <div class="item" @click="filter('Alive')">
          Alive
      </div>
      <div class="item" @click="filter('Dead')">
          Dead
      </div>
      <div class="item" @click="filter('unknown')">
          Unknown
      </div>
  </div>
</template>

<script>
import { useStore } from 'vuex'

export default {
    setup(){
        const store = useStore()

        const filter = ((status) => {
            store.dispatch('filterByStatus', status)
        })

        return {
            filter
        }
    }
}
</script>

<style lang="scss">
.filter {
    width: 400px;
    margin: 0 auto;
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    border-radius: 10px;
    border: 1px solid var(--border-yellow);
    overflow: hidden;
    background-color: var(--background-card);

    .item {
        padding: 1rem 0.5rem;
        text-align: center;
        cursor: pointer;
        &:hover {
            color: var(--text-orange);
            transform: scale(1.2);
        }
    }
}
</style>