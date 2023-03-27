<template>
  <section class="container">
    <h1>The Best Nuxt</h1>
    <p class="subheading">We've got the best nuxt's.</p>

    <p>
      Lorem ipsum dolor sit amet consectetur, adipisicing elit. Voluptates sed
      tenetur quas! Laudantium odio consectetur, quia dolore veritatis quae quam
      nobis aperiam saepe, modi quibusdam facere tenetur omnis earum molestiae.
    </p>

    <b-button variant="outline-primary" @click="changeMess">Button</b-button>

    <div>
      <card :content="mess">
        <h4 slot="header">Card header</h4>
        <h4 slot="footer">Card footer</h4>
      </card>
    </div>
  </section>
</template>

<script>
import Card from "../components/Card.vue";

export default {
  components: { Card },
  data() {
    return {
      mess: "Hello",
      title: "indexPage",
      id: "123",
    };
  },
  name: "IndexPage",
  head() {
    // Set Meta Tags for this Page
    return {
      title: "NUXT Home",
      meta: [
        { name: "description", content: "This is my about description here." },
        { name: "keywords", content: "about nuxt, nuxt info" },
      ],
    };
  },
  methods: {
    changeMess(){
      this.mess = '123'
    }
  },
};
</script>
