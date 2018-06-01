<template lang="pug">
  div(id="app")
    PvNav
    .container
      div.row
        div(v-if="loading") Cargando
        Card(v-for="(pokemon, index) in pokemons", :key="index", :pokemon="pokemon")
        br
      button.btn.btn-success(@click="loadMore", v-if="!loading") Buscar
    PvFooter

</template>

<script>

import Card from '@/components/card'

import PvNav from '@/components/header/nav'
import PvFooter from '@/components/header/footer'

export default {
  name: 'app',

  components: {
    Card,
    PvNav,
    PvFooter
  },
  data () {
    return {
      pokemons: [],
      url: 'https://pokeapi.co/api/v2/pokemon/',
      loading: false
    }
  },

  mounted() {
    this.getPokemon()
  },

  methods: {
    getPokemon() {
      this.loading = true
      fetch(this.url)
      .then(res => res.json())
      .then( res => {
        this.pokemons = res.results,
        this.loading = false,
        this.url = res.next
      })
    },
    loadMore() {
      fetch(this.url)
        .then(res => res.json())
        .then(res => {
          this.pokemons = this.pokemons.concat(res.results) ,
          this.url = res.next
        })
    }
  }
}
</script>

<style>
html {
	min-height: 100%;
	position: relative;
}
body {
  padding-top: 4.5rem;
  margin: 0;
  margin-bottom: 280px;
}

.btn-pv {
  background-color: #00dd4a !important;
}
</style>
