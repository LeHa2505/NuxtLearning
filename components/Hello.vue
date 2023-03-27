<template>
  <div class="children">
    <h2>This is hello component</h2>
    <p>{{msg}}</p>
    <slot><p>This is the fallback content</p></slot>
  </div>
</template>

<script>
export default {
  props: {
    msg: String
  },
  created(){
    // this.$on("click", (msg) => {
    //   this.msg = msg;
    // })
    this.$nuxt.$on('msg-change', (message) => {
      this.msg = message
    })
  }
};
</script>

<style></style>
