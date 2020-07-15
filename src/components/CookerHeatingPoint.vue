<template>
  <svg :x="x" :y="y" :width="width" :height="height">
    <rect x="0" y="0" width="100%" height="100%" fill="red"/>
    <text x="20" y="40">row: {{row}}, col: {{col}}</text>
  </svg>
</template>

<script>
export default {
  name: 'CookerPanel',
  props: ['row', 'col', 'lineLength'],
  data() {
    return {
      width: 250,
      height: 225,
    };
  },
  computed: {
    rowNumber() {
      return parseInt(this.row, 10);
    },
    colNumber() {
      return parseInt(this.col, 10);
    },
    x() {
      return (this.colNumber - 1) * this.width + 20;
    },
    y() {
      return (this.rowNumber - 1) * this.height + 20;
    },
  },
};
</script>
