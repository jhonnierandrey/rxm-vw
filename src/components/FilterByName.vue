<template>
  <div class="search">
      <input type="text" name="" id="" placeholder="Search by name" @keyup="filter()" v-model="name"/>
      <div>
          <i class="fas fa-search"></i>
      </div>
  </div>
</template>

<script>
import { ref } from 'vue'
import { useStore } from 'vuex'
export default {
    setup(){
        const store = useStore()
        const name = ref('')
        const filter = () => {
            store.dispatch('filterByName', name.value)
        }

        return {
            name, filter
        }
    }
}
</script>

<style lang="scss">
.search {
    width: 400px;
    margin: 1rem auto 0;
    border-radius: 10px;
    border: 1px solid var(--border-yellow);
    background-color: rgba(255, 255, 255, 0.5);
    display: flex;

    input {
        height: 53px;
        width: 400px;
        border: none;
        border-radius: 10px;
        padding: 0 0.5rem;
        background-color: transparent;
        color: var(--text-white);

        &:focus-visible {
            outline: none;
        }

        &::placeholder {
            color: var(--text-white);
        }
    }

    div {
        display: flex;
        justify-content: center;
        align-items: center;
        
        .fas {
            font-size: x-large;
            padding-right: 0.5rem;
        }
    }
}
</style>