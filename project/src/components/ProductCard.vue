<template>
  <div class="container_my">
		<div class="img-container">
			<img :src="productDeatils.thumb" alt="img">
		</div>
		<div class="text">
			{{ productDeatils.series }}
		</div>
  </div>
</template>

<script>
 export default{
	name: "ProductCard",
	props: {
		productDeatils: Object
	}
 }

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
	.container_my{	
		color: white;
		width: calc(100% / 6);
		.img-container{
			width: 60%;		
			margin-bottom: 10px;
			margin-top: 20px;
		}
		
	}
</style>