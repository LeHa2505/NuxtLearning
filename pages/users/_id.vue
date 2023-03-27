<template>
  <div>
    jdcjchdj
    <h3>{{ id }}</h3>
  </div>
</template>

<script>
export default {
  name: "blogs",
  data() {
    return {
      id: "hello",
    };
  },
  created() {
    console.log(this.$route.params);
    this.id = this.$route.params.id;
  },
};
</script>
