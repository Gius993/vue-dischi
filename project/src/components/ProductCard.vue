<template>

  <div class="container_my set-color">
		<div class="img-container">
			<img src="https://images.everyeye.it/img-notizie/the-boys-cosa-succede-homelander-incontra-avengers-scopriamolo-insieme-v3-474144-900x900.jpg" alt="prova">
		</div>
		<div class="text">
			<h2>Title</h2>
			<p>testo lalalallalalalallllllllllllll<br>lllllllllllll</p>
		</div>
  </div>
</template>

<script>
 export default{
	name: "ProductCard",
	// props: {
	// 	productDeatils: Object
	// }
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
			width: 70%;	
							
		}
		.text{
			text-align: center;
			margin-top: 20px;
			h2{
				font-size:  50px;
				margin-bottom: 40px;
			}
			p{
				font-size: 25px;
				color: $brand_color_c;
				padding: 20px;
				
			}
		}
		
	}
</style>