<template>
	<div class="contentRegister">
		<input type="text" name="Product" id="produto" placeholder='Digite seu Produto' v-model="product">
		<input type="number" name="Quantity" id="quantidade" placeholder='Digite a Quantidade' v-model="quantity">
		<button id="submit" type="submit" @click="addProduct">Adicionar</button>
	</div>
</template>

<script>

export default {
  name: 'inputProduto',
  data() {
	return {
		product: '',
		quantity: 0
	}
  },
  methods: {
	addProduct() {
		if (!this.product && !this.quantity) {
			return;
		}

		this.$emit('addProduct', {product: this.product, quantity: this.quantity});
	}
  }
}
</script>

<style>
.contentRegister input{
	margin: 10px;
}
</style>
