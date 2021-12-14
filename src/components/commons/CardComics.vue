<template>
  <div class="comicBook">
      <img :src="comicBook.thumb" :alt="comicBook.series">
      <h3>{{comicBook.series.toUpperCase()}}</h3>
  </div>
</template>

<script>
export default {
  name: "CardComics",
  props: {
    comicBook: Object,
  },
};
</script>

<style lang="scss" scoped>
    h3{
        padding-top: 10px;
        font-weight:lighter;
    }
</style>