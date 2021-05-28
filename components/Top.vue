<template>
  <a class="vue-scroll-top" @click="scrollTop">
    <v-icon>fas fa-angle-up</v-icon>
    TOP
  </a>
</template>

<script>
export default {
  methods: {
    scrollTop() {
      this.intervalId = setInterval(() => {
        if (window.pageYOffset === 0) {
          clearInterval(this.intervalId)
        }
        window.scroll(0, window.pageYOffset - 50)
      }, 5)
    },
  },
}
</script>
