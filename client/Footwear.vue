<template>
  <div id="footwear">
    <h3> Footwear </h3>
    <ul id="footwearList">
      <li v-for="item in items" :key="item" @click="selectValue(item)"> {{ item }} </li>
    </ul>  
  </div>  
</template>

<script>
export default {
  name: 'Footwear',
  props: {
    footwear: {
      type: Array
    }
  },
  methods: {
    selectValue(value) {
      this.$emit("selector", { footwear: value })
    }
  },
  data() {
    return {
      items: this.footwear
    }
  }
}
</script>