<template>
  <b-container>
    <b-row>
      <b-col>
        <b-img center class="main_image" src="@/assets/fry.png"></b-img>
      </b-col>
    </b-row>
    <b-row>
      <b-col>
        <div class="heading">{{ msg }}</div>
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
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: "Nunito", sans-serif;
  background: #fbf7f4;
}

.heading {
  text-align: center;
  font-size: 3.5rem;
  font-weight: bold;
  padding: 1rem 0;
}

.counter-container {
  display: flex;
  align-items: center;
}

.counter {
  text-align: center;
}

.counter h3 {
  padding: 0.5rem 0;
  font-size: 2.5rem;
  font-weight: 800;
}

.counter h6 {
  font-size: 2rem;
  padding-bottom: 1rem;
}

.icon {
  height: 5rem;
  width: auto;
}

.main_image {
  max-width: 20rem;
  justify-content: center;
}
</style>
