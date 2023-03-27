<template>
  <div class="card">
    <header class="card-header">
      <slot name="header"></slot>
    </header>

    <div class="card-content">
      <slot><p>{{content}}</p></slot>
       <p>Something</p>
      <b-button variant="outline-primary" @click="callFunction"
        >Button</b-button
      >
    </div>

    <footer class="card-footer">
      <slot name="footer"></slot>
    </footer>
  </div>
</template>

<script>
export default {
  props: {
    content: String
  },
  data() {
    return {
      message: "Message from child",
      mess: ''
    };
  },
  methods: {
    callFunction() {
      this.message = "Message changed";
      this.$nuxt.$emit('msg-change', this.message);
    },
  },
};
</script>

<style></style>
