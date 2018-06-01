<template lang="pug">
  .col-12.col-md-4
    .card.card-cover.text-center
      img.card-img-top.img-pokemon(alt='pokemon', :src="Image", style="width: 100px; height: 100px;")
      .card-body
        h5.card-title {{pokemon.name}}
        button.btn.btn-pv Ver mas de {{pokemon.name}}
</template>

<script>

export default {

  props: {
    pokemon: { type: Object, required: true },
  },
    data () {
      return {
        Image: `https://img.pokemondb.net/artwork/${this.pokemon.name}.jpg`
      }
    }
}
</script>

<style>
 .card {
  width: 100%;
	display: inline-block;
	vertical-align: top;
  margin-bottom: 25px;
  padding: 15px;
 }
</style>

