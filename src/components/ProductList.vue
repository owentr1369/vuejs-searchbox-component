<template>
  <div class="pokemon-list">
    <article v-for="(pokemon, index) in pokemonList" :key="index" class="">
      <h1>{{ pokemon.name }}</h1>
      <img :src="imageUrl + (index + 1) + '.png'" alt="" />
    </article>
  </div>
</template>

<script>
export default {
  data() {
    return {
      pokemonList: [],
      imageUrl:
        "https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/",
    };
  },
  mounted() {
    fetch("https://pokeapi.co/api/v2/pokemon?limit=100000&offset=0")
      .then((res) => res.json())
      .then((data) => {
        this.pokemonList = data.results.slice(0, 400);
        console.log("this.pokemonList :>> ", this.pokemonList);
      });
  },
};
</script>

<style lang="scss">
.pokemon-list {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  grid-gap: 10px;
  width: 100%;
  max-width: 510px;

  article {
    height: 150px;
    background-color: #efefef;
    text-align: center;
    text-transform: capitalize;
    border-radius: 6px;
    cursor: pointer;
    box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2), 0 10px 10px rgba(0, 0, 0, 0.2);
  }
}
</style>