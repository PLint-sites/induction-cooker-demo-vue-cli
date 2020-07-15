<template>
  <div class="home">
    <h1>Induction Cooker</h1>
    <svg viewBox="0 0 1000 1000" xmlns="http://www.w3.org/2000/svg">
        <!-- The light grey background -->
        <rect x="0" y="0" width="100%" height="100%" fill="#dddddd"/>

        <!-- Nest svg for the start of the cooker -->
        <svg x="250" y="100" width="540" height="530">
          <rect x="0" y="0" width="100%" height="100%" fill="black"/>
          <CookerHeatingPoint row="1" col="1" line-length="65"></CookerHeatingPoint>
          <CookerHeatingPoint row="1" col="2" line-length="40"></CookerHeatingPoint>
          <CookerHeatingPoint row="2" col="1" line-length="40"></CookerHeatingPoint>
          <CookerHeatingPoint row="2" col="2" line-length="65"></CookerHeatingPoint>
        </svg>
      </svg>
  </div>
</template>

<script>
import CookerHeatingPoint from '../components/CookerHeatingPoint.vue';

export default {
  name: 'Cooker',
  components: {
    CookerHeatingPoint,
  },
};
</script>
