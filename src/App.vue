<template>
  <Navbar></Navbar>
  <router-view/>
</template>

<style lang="scss">
* {
  box-sizing: border-box;
}

body {
  padding: 0;
}
</style>
<script>
import Navbar from './components/Navbar';

import 'bootstrap/dist/css/bootstrap.min.css';
import 'bootstrap/dist/js/bootstrap.bundle.min.js';

export default {
  components: {Navbar}
}
</script>