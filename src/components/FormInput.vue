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
		quantity: '',
		list: []
	}
  },
  methods: {
	addProduct() {
		if (!this.product && !this.quantity) {
			return;
		}

		this.list.push({product: this.product, quantity: this.quantity});

		this.$emit('addProduct', this.list);

		this.product = '';
		this.quantity = '';
	}
  }
}
</script>

<style>
.contentRegister input{
	margin: 10px;
}
</style>
