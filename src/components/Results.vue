<template>
  <p class="react">reaction time - {{ score }}</p>
  <p class="speed">{{ speed }}</p>
</template>

<script>
export default {
  props: ["score"],
  data() {
    return {
      speed: null,
    };
  },
  mounted() {
    if (this.score < 250) {
      this.speed = "Very fast";
    } else if (this.score < 400) {
      this.speed = "Relatively fast";
    } else {
      this.speed = "Not so fast";
    }
  },
};
</script>

<style>
.speed {
  font-size: 1.4em;
  color: #bd7bcee0;
  font-weight: bolder;
}
.react {
  font-weight: bold;
  color: rgba(0, 119, 128, 0.76);
}
</style>
