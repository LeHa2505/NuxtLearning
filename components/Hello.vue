<template>
  <div class="children">
    <h2>This is hello component</h2>
    <p style="font-weight: bold">Before: {{text}}</p>
    <p style="font-weight: bold">After: {{reverseText()}}</p>
    <slot><p>This is the fallback content</p></slot>
    <p>{{msg}}</p>
  </div>
</template>

<script>
export default {
  props: {
    msg: String, 
    text: String
  },
  created(){
    // this.$on("click", (msg) => {
    //   this.msg = msg;
    // })
    this.$nuxt.$on('msg-change', (message) => {
      this.msg = message
    })
  },
  methods: {
    reverseText(){
      return this.text.split(" ").reverse().join(" ");
    }
  }
};
</script>

<style></style>
