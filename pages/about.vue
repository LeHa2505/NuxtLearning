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
      <hello>
        <p>Helloooooooooooooooo</p>
      </hello>
    </div>

    <card >
      <h4 slot="header">Card header</h4>
      <p slot-scope="props" v-text="props.content"></p>
      <h4 slot="footer">{{content}}</h4>  
    </card>
  </section>
</template>

<script>
import Card from "../components/Card.vue";
import Hello from "../components/Hello.vue";
export default {
  components: { Hello, Card },
  props: {
    content: String,
  },
  created(){
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
  }
  // transitions: 'bounce'
};
</script>
