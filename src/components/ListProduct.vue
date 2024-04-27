<template>
	<div class="containerList">
		<div v-for="(item, index) in products" :key="index">
			{{item.product}}
			{{item.quantity}}
		</div>
	</div>
</template>

<script>

export default {
  name: 'inputProduto',
  props: {
	products: Array
  }
}
</script>

<style>

</style>
