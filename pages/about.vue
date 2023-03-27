<template>
  <section class="container">
    <h1>About our Nuxt's</h1>
    <p class="subheading">They're juicy and stuff.</p>

    <p>
      Lorem ipsum dolor sit amet consectetur, adipisicing elit. Voluptates sed
      tenetur quas! Laudantium odio consectetur, quia dolore veritatis quae quam
      nobis
    </p>

    <div>
      <hello :text="text">
        <p>Hello part</p>
      </hello>
      <b-button variant="outline-primary" @click="changeName">Button</b-button>
    </div>

    <card>
      <h4 slot="header">Card header</h4>
      <p slot-scope="props" v-text="props.content"></p>
      <h4 slot="footer">{{ content }}</h4>
    </card>
  </section>
</template>

<script>
import Card from "../components/Card.vue";
import Hello from "../components/Hello.vue";
export default {
  components: { Hello, Card },
  props: {},
  data() {
    return {
      text: "Text here",
    };
  },
  created() {
    this.content = "From about page";
  },
  head() {
    return {
      title: "About Nuxt",
      meta: [
        { name: "description", content: "This is my about description here." },
        { name: "keywords", content: "about nuxt, nuxt info" },
      ],
    };
  },
  methods: {
    changeName() {
      this.text = "Text has been changed";
    },
  },
  // transitions: 'bounce'
};
</script>
