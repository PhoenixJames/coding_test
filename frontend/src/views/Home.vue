<template>
  <div class="home">
    Home Page
  </div>
</template>

<script>
import data from '@/assets/data/res_data.js';

export default {
  name: 'Home',
  components: {
  },
  mounted() {
    console.log({ data });
  },
};
</script>
