<template>
  <div>
    <h3> Tops </h3>
    <ul>
      <li v-for="item in items" :key="item" @click="selectValue(item)"> {{ item }} </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Tops',
  props: {
    tops: {
      type: Array
    },
    selector: {
      type: Function
    }
  },
  methods: {
    selectValue(value) {
      this.$emit("selector", { tops: value })
    }
  },
    
  data() {
    return {
      items: this.tops

    }
  },
}
</script>