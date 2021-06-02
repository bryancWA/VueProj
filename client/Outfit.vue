<template>
  <div id="outfit">
    <h3>Your Outfit For Today: </h3>
    <h4> {{ outfit.tops }} </h4>
    <h4> {{ outfit.bottoms }} </h4>
    <h4> {{ outfit.footwear }} </h4>
  </div>
</template>

<script>
export default {
  name: 'Outfit',
  props: {
    outfitObj: Object
  },
  data() {
    return {
      outfit: this.outfitObj
    }
  }
}
</script>