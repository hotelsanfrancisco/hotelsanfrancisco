<template>
  <div class="col">
    <div class="card h-100">
      <g-image :src="setImage" class="card-img-top" />
      <div class="card-body">
        <div class="h3">
          {{ title }}
        </div>
        <div class="note">Desde {{ price }} pesos</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: ["title", "image", "price"],
  computed: {
    setImage: function () {
      return require("~/assets/photos/" + this.image);
    },
  },
};
</script>

<style lang="scss" scoped>
.card {
  border-radius: 8px;
}
// .card-img-top {
//   height: 200px;
//   width: 100%;
//   display: block;
// }
.card-body .h2 {
  margin: 0;
}
</style>