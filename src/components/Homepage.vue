<template>
  <b-container fluid="sm">
    <b-row>
      <b-col>
        <b-img class="status_image" src="@/assets/fry.png"></b-img>
        <h1>{{ msg }}</h1>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
export default {
  name: 'Homepage',
  props: {
    msg: String
  }
}
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

.status_image {
  max-width: 256px;
}
</style>
