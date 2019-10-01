<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <button v-on:click="increment">
      Click me
    </button>
    {{ a }}
    {{ b }}
    <div>
    </div>
  </div>
</template>

<script>
var HelloWorld = {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data: function () {
    return {
      a: 0
    };
  },
  methods: {
    increment: function() {
      this.a += 1;
    }
  },
  computed: {
    b: function () {
      return this.a - 1;
    }
  }
};
export default HelloWorld;
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
