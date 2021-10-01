<template>
  <p>Reacion Time : {{ score }}ms</p>
  <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
  props: ["score"],
  data() {
    return {
      rank: null,
    };
  },
  mounted() {
    if (this.score < 250) {
      this.rank = "Godlike";
    } else if (this.score < 400) {
      this.rank = "Fair enough";
    } else {
      this.rank = "Hi grandpa!";
    }
  },
};
</script>

<style>
.rank {
  font-size: 1.4em;
  font-weight: bold;
  color: #0faf87;
}
</style>