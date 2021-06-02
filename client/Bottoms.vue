<template>
  <div>
    <h3> Bottoms </h3>
    <ul>
      <li v-for="item in items" :key="item" @click="selectValue(item)"> {{ item }} </li>
    </ul>

  </div>
</template>

<script>
export default {
  name: 'Bottoms',
    props: {
      bottoms: {
        type: Array
      }
  },
  methods: {
    selectValue(value) {
      this.$emit("selector", { bottoms: value })
    }
  },
  data () {
    return {
      items: this.bottoms
    }
  }
}
</script>