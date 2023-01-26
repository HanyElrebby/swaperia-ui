<template>
  <Navbar @hide="hideScroll"/>
</template>

<script>
import Header from './views/Header.vue'
import Navbar from './views/Navbar.vue'


export default {
  data() {
    return {
    }
  },
  components: {
    Header,
    Navbar
},
  methods: {
    hideScroll(data) {
      console.log(data)
      if (data) {
        document.body.classList.add('hide')
      } else {
        document.body.classList.remove('hide')
      }
    }
  }
}
</script>

<style>
.hide {
  overflow: hidden;
}
</style>