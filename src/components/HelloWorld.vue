<template>
  <div class="hello">
    <p>{{ data }}</p>
    <button @click="getPosts">Get posts</button>
  </div>
</template>

<script>
import axios from "axios";

export default {
	name: "HelloWorld",
	data() {
		return {
			data: null,
		};
	},
	methods: {
		async getPosts() {
			this.data = await axios.get("https://testeb.ozlive.io/");
			console.log({test: this.data});
		},
	},
};
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
