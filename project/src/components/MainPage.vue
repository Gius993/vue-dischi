<template>
  <div class="container">
		<div class="container_card">
			<ProductCard />
			<ProductCard />
			<ProductCard />
			<ProductCard />
			<ProductCard />
			<ProductCard />
			<ProductCard />
			<ProductCard />
			<ProductCard />
			<ProductCard />

		</div>
		
  </div>
</template>

<script>
import ProductCard from "./ProductCard";
export default {
  name: 'MainPage',
  components: {
	ProductCard,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
	@import  '../style/variables.scss';

	.container{
		background-color:$brand_color_b;
		width: 100%;
		height: 100vh;
		padding: 0 25%;
		display: flex;
		align-items: center;
	}
		
	.container_card{
		display: flex;
		flex-wrap: wrap;			
	}
</style>