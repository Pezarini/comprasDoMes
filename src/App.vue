<template>
	<div id="app">
		<div class="header">
			<h1>Lista de Compras</h1>
		</div>

		<div class="formInput">
			<FormInput @addProduct="products = $event"/>
		</div>

	</div>
</template>

<script>
import FormInput from './components/FormInput.vue'

export default {
  name: 'App',
  data() {
	return {
		products: []
	}
  },
  components: {
    FormInput
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
