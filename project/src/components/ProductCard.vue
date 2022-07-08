<template>

  <div class="container_my set-color">
		<div class="img-container">
			<img :src="info.poster" :alt="info.name">
		</div>
		<div class="text">
			<h2>{{ info.title }}</h2>
			<p>{{ info.author }} {{ info.genere }} {{ info.year }}</p>
		</div>
  </div>
</template>

<script>
 export default{
	name: "ProductCard",
	props: ['info']
 }

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
	@import  '../style/variables.scss';
	.set-color{
		color: white;
		background-color:$brand_color_a;

	}
	.container_my{	
		width: calc(100% / 5 - 20px);
		padding-top: 20px;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		margin-bottom: 50px;
		margin-left:20px;
		
		.img-container{
			width: 100%;	
			padding: 20px;						
		}
		.text{
			text-align: center;
			margin-top: 20px;
			
			h2{
				font-size:  30px;
				margin-bottom: 10px;
			}
			p{
				font-size: 20px;
				color: $brand_color_c;
				padding: 20px;
				
			}
		}
		
	}
</style>