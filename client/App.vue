

<template>
  <div id="app">
    <h2> Your Wardrobe Consists Of: </h2>
    <Tops 
      :tops="items.tops"
      @selector="handleSelector"
    />
    <Bottoms 
      :bottoms="items.bottoms"
      @selector="handleSelector"
      />
    <Footwear 
      :footwear="items.footwear"
      @selector="handleSelector"
      />
    <Outfit 
      :outfitObj="this.state"
    />
  </div>
</template>

<script>
import Footwear from './Footwear.vue';
import Tops from './Tops.vue';
import Bottoms from './Bottoms.vue';
import Outfit from './Outfit.vue';




export default {
  data() {
    return {
      state: {
        tops: '',
        bottoms: '',
        footwear: ''
      },
      items: {
        tops: [
          'Long-sleeve Shirt',
          'Tank-top',
          'Shirtless'
        ],
        bottoms: [
          'Pants',
          'Shorts',
          'Underwear'
        ],
        footwear: [
          'Boots',
          'Sandals',
          'Oxfords'
        ]
      },

    }
  },
  components: {
    Tops,
    Bottoms,
    Footwear,
    Outfit
  },
  methods: {
    handleSelector(value) {
      // console.log('you clicked:', value);
      for (var key in value) {
        if (key === 'tops') {
          // console.log("tops", value.tops);
          this.state.tops = value.tops;
        }
        if (key === 'bottoms') {
          this.state.bottoms = value.bottoms;
        }
        if (key === 'footwear') {
          this.state.footwear = value.footwear;
        }
      }
      // console.log('state obj', this.state)

    }
  }
}
</script>

<style>

</style>


