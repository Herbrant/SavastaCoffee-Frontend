<template>
  <b-container fluid="sm">
    <b-row>
      <b-col cols="sm-4" class="mx-auto">
        <b-card title="test">
			<b-card-body>
				<p>Coffee:</p>
				<p>Status:</p>
			</b-card-body>
		</b-card>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
export default {
  name: 'Maincard',
  props: {
    title: String,
	body: String
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
</style>
