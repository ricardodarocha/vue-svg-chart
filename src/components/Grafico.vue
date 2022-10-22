<template>
  <div class="grafico">
    <svg height="600" >
      <g 
      v-for="(value, i) in serie1" v-bind:key="i" 
      :transform="`translate(0, ${i * 16})`">
      <rect
        v-bind:x="x_value"
        v-bind:y="y_value"
        v-bind:width="barWidth(value)"
        v-bind:height="h_value"
        v-bind:fill="color"
      />
      <text y="15">{{value}} {{key}}</text>
    </g>
    </svg>
  </div>
</template>

<script>
export default {
  name: 'Grafico',
  props: {
    x: Number,
    y: Number,
    h: Number,
    w: Number,
    color: String
  },
  data() {
    return {
      serie1: [8, 5, 7, 9, 13, 15, 14, 8, 9, 13],
      serie2: [5, 7, 9, 5, 7, 12, 14, 8, 5, 1],
      x_value: 0,
      y_value: 0,
      h_value: 12,
      w_value: 150,
    }
  },
  methods: {
    barWidth(value) { return value * 20 }
  },
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
